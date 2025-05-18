# fine-tuning-GPT2-for-chat-bot
Fine-tuned a large language model for chatbot Q&amp;A using supervised learning on the Chatbot Arena dataset. Explores parameter-efficient fine-tuning (PEFT) with LoRA, Adapters, Prompt &amp; Prefix Tuning. Ideal for safe, fast adaptation of large models on small data
#  Supervised Fine-Tuning of LLMs with PEFT

This project demonstrates how to fine-tune a Large Language Model (LLM) using **supervised learning** with labeled chatbot conversations. It also explores **Parameter-Efficient Fine-Tuning (PEFT)** methods like LoRA and prompt tuning to make the process efficient, safe, and scalable.

---

##  What Is Supervised Fine-Tuning?

Supervised fine-tuning is the process of training a pretrained language model on a **task-specific labeled dataset**. This enables the model to perform more specialized tasks like:
- Answering questions
- Writing scripts
- Translating languages

While base models are trained to predict the next token, **fine-tuned models understand task structure** and respond accurately to prompts.

---

##  Parameter-Efficient Fine-Tuning (PEFT)

PEFT techniques allow large models to be fine-tuned **without updating all parameters**. This saves memory, speeds up training, and avoids overfitting on small datasets.

###  Key PEFT Methods

| Method | Description |
|--------|-------------|
| **LoRA** | Injects trainable low-rank matrices into pretrained weights |
| **Adapters** | Adds small neural modules between layers |
| **Prompt Tuning** | Learns soft prompt tokens prepended to input |
| **Prefix Tuning** | Learns key/value vectors prepended to transformer layers |

**Why PEFT?**  
It is:
- Memory efficient
- Faster to train
- Less prone to overfitting
- Safer for small data and large models

---

## Project Overview

- **Dataset**: `lmsys/chatbot_arena_conversations`  
  A labeled dialogue dataset from multiple chatbots and human interactions.

- **Training Setup**:
  - Input format includes tokens like `### Human:` and `### Assistant:` to separate Q&A parts.
  - Injects both question and answer into the model simultaneously.
  - Encourages context alignment during training.

---

 Author
Razieh Moradi Graduate Student, McMaster University  moradr1@mcmaster.ca
