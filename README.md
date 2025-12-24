Synthetic Streak Flow Simulation

This project generates synthetic streak-based images, applies multiple noise models, and visualizes motion using velocity vectors. It is designed as a controlled environment for experimenting with image noise, intensity variation, and flow visualization using Node.js and the Canvas API.

The code is intended for simulation, visualization, and prototyping rather than real-world image analysis.

Features

Synthetic streak generation with intensity gradients

Background speckle and low-intensity noise

Multiple noise models including:

Uniform noise

Gaussian-like noise

Salt-and-pepper noise

Periodic banding

Compression-style block artifacts

Simulated motion blur

Illumination and glare effects

Conceptual denoising by regenerating clean signals

Velocity vector visualization derived from streak geometry

Particle-based flow field simulation with curved motion paths

Project Structure

The repository contains several independent scripts, each focusing on a specific concept:

Base streak generation
Creates vertical streaks with randomized position, length, width, and intensity.

Noise simulation
Adds layered synthetic noise to simulate imaging artifacts.

Intensity variation experiments
Focuses on overlapping streaks and wider intensity ranges.

Velocity vector visualization
Draws motion vectors based on streak direction and intensity gradients.

Curve fitting / flow field simulation
Uses particles moving through a continuous flow field to generate curved streaks and true velocity vectors.

Each script saves its output as a PNG image for inspection.

Requirements

Node.js (v16 or later recommended)

canvas npm package (node-canvas)

A system with Cairo dependencies installed
(required by node-canvas)

Installation

Clone the repository and install dependencies:

git clone https://github.com/your-username/synthetic-streak-flow.git
cd synthetic-streak-flow
npm install


If canvas fails to install, make sure the required native dependencies are installed for your operating system.

Usage

Run any script directly with Node.js:

node script-name.js


Each script will generate one or more PNG files in the project directory, such as:

stage1_base_streaks.png

stage2_noisy_image.png

stage3_denoised_image.png

stage4_final_vectors.png

output.png

You can modify parameters like canvas size, number of streaks, or noise strength directly in the scripts.

Notes on Denoising and Flow

The denoising step is conceptual and implemented by regenerating the clean signal, not by filtering noisy data.

In streak-based scripts, velocity vectors are inferred from known streak geometry.

In the particle-based flow simulation, vectors come from an explicit flow field and represent true motion.

Intended Use

This project is useful for:

Testing visualization techniques

Simulating noisy imaging environments

Prototyping motion and flow representations

Educational demonstrations of synthetic data generation

It is not intended as a production optical flow or image processing library.
