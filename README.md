
# 2D Ising Model Explorer 🧲  
**Advanced Monte Carlo, Cluster Updates, Error Bars, Histograms, Spin-State Animation**

------

## Overview

Simulate, visualize, and analyze the physics of the 2D Ising model—**the classic playground for phase transitions and magnetism**—using a fast, research-level, and easy-to-use Streamlit dashboard powered by [JAX](https://github.com/google/jax).  
This app features:

- **Three update algorithms**: single-spin (Metropolis), modern JAX checkerboard, and cluster (Wolff) MC.
- **Detailed plots**: Magnetization and heat capacity, with error bars and experiment overlay.
- **Automatic phase diagrams** with live spin-state snapshots.
- **Magnetization histograms** at any temperature.
- **Animated GIFs**: Watch spin evolution and see the phase transition LIVE!
- **Step-by-step, tab-by-tab scientific explanations**—learn, teach, and publish.

------

## Features

- **Material selector** (iron, K2CoF4, etc.; extend as you like).
- **All simulation and MC parameters, fully interactive** (lattice size, steps, samples, etc.).
- **Toggle MC algorithm** for teaching/research: Cluster (Wolff), Metropolis, JAX checkerboard.
- **In-depth tab explanations**: Each tab explains the physics and what the plot/animation means.
- **Magnetization/heat capacity with error bars** (true statistical mechanics!).
- **Upload experimental data** and automatically compare with simulation (RMSE shown).
- **Probability histograms**: See critical fluctuations at $T_c$.
- **Dynamic animations**: Real-time GIFs of spin evolution and temperature sweeps.
- **Bilingual usage guide (Eng/Hindi)** and rich markdown for user orientation.

------

## Quickstart

1. **Install requirements:**
    ```bash
    pip install streamlit jax jaxlib numpy matplotlib pandas imageio
    ```
    - **For GPU**: Install [JAX with CUDA/ROCm as per official JAX docs](https://github.com/google/jax#installation).

2. **Save the Python code as** `ising_explorer.py`.
3. **Start the app:**
    ```bash
    streamlit run ising_explorer.py
    ```
4. **Set parameters and run your simulation!**
    - Navigate all results via the tabbed interface.
    - Experiment with cluster MC, temperature range/lattice size, histogram T, and more.
    - See in-app guide and per-tab explanations as you explore.

------

## Usage Guide

- **Sidebar**: Set material, algorithm, N, MC steps, temperature range, and seed.
- **Tabs**:
    1. *Magnetization vs Temperature*: See phase transition; error bars quantify uncertainty; compare with experiment.
    2. *Heat Capacity vs Temperature*: Critical peak locates $T_c$; scientific interpretation given below.
    3. *Phase Diagram*: Regions, phase boundary, and true lattice snapshots (visualizes order/disorder!).
    4. *Histogram*: Understand order parameter distribution and criticality—see phase coexistence.
    5. *Animations*: Watch domains grow, melt, and see real-time statistical physics in motion.
- **Upload**: Drop in your own `T[K], M[]` CSV (optional).
- **Export**: Download results, save GIFs/figures for research or lectures.

------

## File Structure

```
ising_explorer.py             # The main Streamlit/JAX app
README.md                     # This file
requirements.txt              # All Python dependencies
spin_evolution.gif            # Example output (generated)
ising_temp_sweep.gif          # Example output (generated)
```

------

## Requirements (For requirements.txt)

```
streamlit
jax
jaxlib
numpy
matplotlib
pandas
imageio
```
*(If using GPU, follow JAX official install instructions for jaxlib)*

------

## FAQ & Tips

- **How do I make the curves smoother?**
    - Increase "Lattice Size" ($N$), "Equilibration Steps", and "Samples per T" in Sidebar.
- **What’s the difference between MC algorithms?**
    - Checkerboard = JAX/NumPy fast (default, fine for most phases).
    - Metropolis = Standard textbook MC.
    - Wolff Cluster = Best/fastest near $T_c$ for criticality and finite-size research.
- **Where is the science explained?**
    - Read each tab! All graphs, histograms, and animations have detailed, per-plot guidance and physics explanations.
- **Where are simulations saved?**
    - Animations (`.gif`) are saved to run directory; plots can be saved from the Streamlit image display.

------

## Learning Goals

- **See**: Spontaneous symmetry breaking, critical fluctuations, and order-to-chaos transition in magnetic systems.
- **Learn**: Key ideas in phase transitions, why and how MC/cluster algorithms are used, and how order/disorder show up in real, simulated, and experimental data.
- **Experiment**: Try different $N$, MC settings, compare algorithm speeds, and overlay real measurements for science insight.

------

## Credits

- Core MC, cluster, and plotting algorithms: Statistical mechanics literature (Onsager, Wolff MC, classic Ising textbooks)
- JAX/Streamlit integration: This app
- Science communication and UI: [Your Name/Lab/Institution]

------

## License

MIT License (adapt for teaching/research/publishing, with citation/acknowledgement)

------

## Screenshots

Add your own simulation screenshots here!

------

## References

- Statistical Mechanics: Pathria, Huang, Plischke & Bergersen
- [Wolff Algorithm](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.62.361)
- [JAX project (Google)](https://github.com/google/jax)
- [Streamlit dashboard framework](https://streamlit.io/)

------

**Enjoy discovering the beauty of phase transitions and magnetism—visually, interactively, and scientifically!**
```

---

**Want this as a text or markdown file? Just copy the above and save as `README.md`.**  
You can tweak author/citation, add your logo, and upload sample GIF/figures for a complete scientific app distribution.

Citations:
[1] 1000011967.jpg https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/images/77828185/72478d71-2d89-437f-abcd-5c3e8c1f23a8/1000011967.jpg
