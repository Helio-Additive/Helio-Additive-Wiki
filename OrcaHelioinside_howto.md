# Helio Additive OrcaSlicer Integration for Thermal Simulation

This document provides instructions on how to use the Helio Additive integration with OrcaSlicer for performing thermal simulations on G-code for 3D printed parts.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [FAQ](#faq)
- [Contributing](#contributing)

---

## Overview

The Helio Additive integration with OrcaSlicer enables users to simulate the thermal performance of 3D printed parts directly from the G-code. This tool helps in predicting heat distribution and potential thermal issues during the printing process, ultimately allowing process engineers and 3D printing enthusiasts better interpretability of process settings and improved print quality, print time, and part performance.

---

## Prerequisites

- **OrcaSlicer Helio Inside**: Install OrcaSlicer with the Helio Inside app according to your OS workflow.
- **Supported Filament and Printer Presets**:  
  Download the Helio filament and printer presets package, extract, and import into OrcaSlicer:  
  `File >> Import >> Import configs...` and select the filament you wish to use.

> **Note**: The presets are based on existing OrcaSlicer profiles. Helio adds the necessary filament/printer IDs so our backend recognizes them for correct simulation.

---

## Usage

### 1. Open OrcaSlicer and Set Up Your API Key

Each user receives a unique API key to authenticate. You can obtain a key either:

- From Helio Additive directly, or
- By registering via the [Helio Additive dashboard](https://your-dashboard-url.com) and generating one from your user profile page.

Paste your API key in OrcaSlicer via:  
`Settings/Preferences` → Scroll to the bottom → Enter API key.

---

### 2. Import Presets

Import both the **printer** and **filament** presets from the Helio-supported presets package.

---

### 3. Set Up Slice Settings As Normal

Use your typical slicing configurations.

---

### 4. Set Up Your Helio Ambient Settings

For accurate thermal simulation, input the ambient temperature of your build chamber:

- Go to the **Printer Settings UI** → **Basic Information** tab.
- Enter the environment temperature in the **Initial air temperature** field.
- Units are in °C.

> For example: On the **Bambu Lab X1E**, set this to match your chamber setpoint.

---

### 5. Slice Plate Normally

Use the "Slice Plate" button to generate a standard G-code. Make any necessary adjustments before running a simulation.

---

### 6. Slice with Helio

Click the drop-down next to **Slice Plate** → choose **Slice**
