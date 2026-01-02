# Rapid7_IDR_Query_assistant
A lightweight GenAI-powered assistant that converts natural language security questions into valid Rapid7 InsightIDR SIEM queries using Gemini LLM, with strict schema enforcement.

What It Does

Accepts natural language SIEM queries

Generates single-line, valid InsightIDR queries

Enforces allowed fields, operators, and logic

Rejects non-security-related questions safely

Web UI built with Streamlit

Architecture

User → Streamlit UI → Gemini LLM (system prompt + schema) → InsightIDR Query

Key Features

Deterministic output (temperature = 0.0)

Schema-restricted query generation

Hallucination-resistant prompt design

Security-first guardrails

Easy to extend for SOAR / SIEM automation

Tech Stack

Python 3.9+

Streamlit

Google Gemini API

Prompt-based schema validation
