GitHub Repository Setup – Community Building Task

Repository Name:

genlayer-workshop-materials

Repository Description:

Hands-on workshop materials for onboarding developers to GenLayer, including Python Intelligent Contracts, frontend integration with genlayer-js, and tutorial resources.


---

README.md Content

# GenLayer Workshop Materials

Welcome to the GenLayer workshop repository! This repo contains hands-on materials to help new developers learn how to build dApps on GenLayer.

## Contents
- `Workshop_Tutorial.md` → Step-by-step guide for building a Python Intelligent Contract and connecting it with a frontend using genlayer-js.
- `examples/` → Sample Python contracts and frontend snippets.
- `slides/` → Workshop slides (optional).

## Goal
This repository is designed to onboard developers to GenLayer by providing tutorials, code examples, and practical exercises demonstrating:
- Optimistic Democracy Consensus
- Equivalence Principle
- GenLayer Studio usage
- Python Intelligent Contracts
- Frontend integration with genlayer-js


---

Workshop_Tutorial.md Content

# GenLayer Workshop Tutorial

## Introduction
Welcome to the GenLayer workshop! This tutorial will guide you through building your first dApp using GenLayer. Key concepts include:
- Optimistic Democracy Consensus
- Equivalence Principle
- GenLayer Studio
- Python Intelligent Contracts
- Frontend integration with genlayer-js

## Part 1: Setting Up the Project
1. Fork the GenLayer boilerplate: https://github.com/genlayerlabs/genlayer-project-boilerplate
2. Clone your fork:
   ```bash
   git clone <your-fork-url>
   cd genlayer-project-boilerplate
   pip install -r requirements.txt

3. Explore folders:

contracts/ → Python contracts

frontend/ → frontend code




Part 2: Writing a Python Intelligent Contract

Create contracts/dispute_contract.py:

from genlayer import Contract, State

class DisputeContract(Contract):
    state = State()

    def submit_dispute(self, user, issue):
        self.state[user] = issue

    def resolve_dispute(self, user, resolution):
        if user in self.state:
            self.state[user] = resolution
            return True
        return False

Part 3: Frontend Integration with genlayer-js

Install genlayer-js:

npm install genlayer-js

Example frontend/index.js:

import { GenLayerContract } from "genlayer-js";

const contract = new GenLayerContract("DisputeContractAddress");

// Submit a dispute
await contract.submit_dispute("Alice", "Issue description");

// Resolve a dispute
await contract.resolve_dispute("Alice", "Resolution outcome");

Part 4: Testing & Deployment

Deploy in GenLayer Studio

Test submitting and resolving disputes

Observe Optimistic Democracy in action


Conclusion

By completing this workshop, attendees can confidently build and deploy dApps on GenLayer, understanding core concepts and tools.

---

## **Optional Folders**
- `examples/` → Python contract snippets, frontend JS snippets  
- `slides/` → PDF or images of workshop slides for demonstration  

---

# **Portal Submission – Community Building Task**

**Description (350–400 characters):**

Organized and participated in a GenLayer workshop introducing developers to building dApps. Explained key concepts like Optimistic Democracy and Intelligent Contracts, guided attendees through Python Intelligent Contracts and frontend integration using genlayer-js, and provided real-time technical assistance.

**Optional Extended Description:**

Led a hands-on workshop to onboard new developers to GenLayer. Delivered step-by-step tutorials on writing Python Intelligent Contracts, integrating them with a frontend using genlayer-js, and deploying dApps on GenLayer Studio. Provided technical assistance and ensured attendees successfully learned and applied key concepts.

**Evidence / Supporting Info:**

GitHub repository containing all workshop materials: https://github.com/<your-username>/genlayer-workshop-materials (Optional) Screenshots, slides, or recordings of the workshop
