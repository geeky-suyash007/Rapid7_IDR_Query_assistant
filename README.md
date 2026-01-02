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


Example Input / Output

Input:
Show high severity malware alerts

Output:
where(severity="High" AND signature_name CONTAINS "MALWARE")

Setup
pip install streamlit google-generativeai
streamlit run app.py


Set API key:

export GOOGLE_API_KEY="your_api_key"

Use Cases

SOC analyst query assistance

SIEM query standardization

LLM-safe security automation

SOAR pipeline integration



Disclaimer

For query generation only. Always validate queries before production use.

