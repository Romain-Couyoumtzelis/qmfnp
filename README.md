# qmfnp

Explorations of quantum states and dynamics across a few focused Jupyter notebooks: Bloch-sphere intuition with Pauli expectations, rotating-frame analytics, harmonic-oscillator eigenstates and wavepacket evolution, and two‑qubit Pauli vectors and Hamiltonian analysis.

## Quick links
- Notebooks:
  - [HMW1 p1/homework1_part1.ipynb](./HMW1%20p1/homework1_part1.ipynb)
  - [HMW1 p2/homework1_part2.ipynb](./HMW1%20p2/homework1_part2.ipynb)
  - [HMW2/homework2.ipynb](./HMW2/homework2.ipynb)
  - [HMW3/homework3.ipynb](./HMW3/homework3.ipynb)
- PDFs:
  - [HMW1 p1 Questions](./HMW1%20p1/Homework%201%20part%201%20Questions.pdf)
  - [HMW1 p2 Questions](./HMW1%20p2/Homework%201%20part%202%20Questions.pdf)
  - [HMW2 Questions](./HMW2/Homework%202%20Questions.pdf)
  - [HMW2 Solutions](./HMW2/Homework%202.pdf)
  - [HMW3](./HMW3/Homework%203.pdf)

## Animations
- Google Drive:
  - Gaussian evolution: https://drive.google.com/file/d/1xBMc4BVwg_NiMq4R7nTty38XURFmKp-U/view?usp=drive_link
  - Coherent state evolution: https://drive.google.com/file/d/1M9lmi302z-evt-ZlCJFYi3FjpTfC4vHC/view?usp=drive_link
  - Superposition evolution: https://drive.google.com/file/d/1-wvRYg7IA4UM-jpUwc7rdimFDQxL7v0g/view?usp=drive_link
- In repo (HMW2):
  - [wavepacket_evolution.mp4](./HMW2/wavepacket_evolution.mp4)
  - [wavepacket_evolution_coherent_state.mp4](./HMW2/wavepacket_evolution_coherent_state.mp4)
  - [wavepacket_evolution_superposition.mp4](./HMW2/wavepacket_evolution_superposition.mp4)

## Description

- HMW1 p1:
  - Bloch-sphere view of a single qubit. Derives and validates ⟨ψ|σz|ψ⟩ = cos(θ) and ⟨ψ|σx|ψ⟩ = sin(θ) numerically with QuTiP, plus 3D surfaces over (θ, φ). Demonstrates the effect of a Hadamard gate on states and axes.
- HMW1 p2:
  - Symbolic linear algebra with SymPy: eigenvalues/eigenvectors, closed‑form matrix exponentials, and a rotating-frame transformation for two-level systems; builds unitaries U and U′ for time evolution.
- HMW2:
  - Harmonic oscillator. Constructs ψn(x) via the ladder‑operator recurrence, checks normalization with SciPy quad, verifies orthogonality, and visualizes |ψn|² with energy levels. Includes wavepacket animations (Gaussian, coherent, superposition).
- HMW3:
  - Two‑qubit circuits and Pauli vectors with Qiskit. Builds |+−⟩ and Bell states, plots PauliVec, and analyzes a coupled two‑qubit Hamiltonian (eigs/eigvecs, time evolution, measurement probabilities).

## Interesting techniques

- Expectation values with QuTiP’s operators and states; overlays against closed forms to validate numerics.
- 3D surfaces for expectation landscapes using Matplotlib’s mplot3d (see [Matplotlib mplot3d docs](https://matplotlib.org/stable/api/toolkits/mplot3d.html)).
- Symbolic matrix exponentials and rotating-frame transforms with SymPy ([Matrix.exp](https://docs.sympy.org/latest/tutorial/matrices.html#matrix-exponential)).
- Ladder-operator recurrence to generate Hermite functions ψn(x) without directly calling orthogonal polynomials; normalization and overlap via [SciPy integrate.quad](https://docs.scipy.org/doc/scipy/reference/generated/scipy.integrate.quad.html).
- Wavepacket movies with [Matplotlib Animation writers](https://matplotlib.org/stable/api/animation_api.html).
- Pauli-vector projections for multi-qubit states (Qiskit plot_state_paulivec), alongside manual density‑matrix traces for verification.
- Auto‑generated HTML/JS for notebook animations:
  - Range input: [MDN input type="range"](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range)
  - Event handling: [addEventListener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
  - Timing: [setInterval/clearInterval](https://developer.mozilla.org/en-US/docs/Web/API/setInterval)
  - Image preloading: [HTMLImageElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/Image)

## Non‑obvious libraries and choices

- QuTiP and QuTiP-QIP for quantum operators, circuits, and Bloch visualizations:
  - [QuTiP](https://qutip.org/)
  - [QuTiP‑QIP](https://qutip-qip.readthedocs.io/)
- SymPy for exact linear algebra, eigendecompositions, and exp(M t): [SymPy docs](https://docs.sympy.org/)
- Qiskit for state construction, circuit drawing, and PauliVec: [Qiskit](https://qiskit.org/) (PauliVec: [plot_state_paulivec](https://docs.quantum.ibm.com/api/qiskit/visualization#plot_state_paulivec))
- SciPy integrate.quad for continuous normalization/overlap checks on ψn: [SciPy docs](https://docs.scipy.org/doc/scipy/reference/generated/scipy.integrate.quad.html)
- ipywidgets for notebook interactivity (sliders, controls): [ipywidgets](https://ipywidgets.readthedocs.io/)

## External libraries and fonts

- Jupyter Notebook: [Jupyter](https://jupyter.org/)
- NumPy: [NumPy docs](https://numpy.org/doc/stable/)
- SciPy: [SciPy docs](https://docs.scipy.org/doc/scipy/)
- Matplotlib: [Matplotlib](https://matplotlib.org/stable/)
- SymPy: [SymPy docs](https://docs.sympy.org/)
- QuTiP: [QuTiP](https://qutip.org/)
- Qiskit: [Qiskit](https://qiskit.org/)

Fonts
- Uses Matplotlib defaults unless configured; see [Matplotlib font management](https://matplotlib.org/stable/tutorials/text/text_props.html#customizing-fonts)

## Project structure

```
/
├─ HMW1 p1/
├─ HMW1 p2/
├─ HMW2/
├─ HMW3/
├─ README.md
├─ .DS_Store
```

## Notes
- HMW1 p1: Single‑qubit Bloch sphere, Pauli expectations, Hadamard demo. See [homework1_part1.ipynb](./HMW1%20p1/homework1_part1.ipynb).
- HMW1 p2: SymPy eigen/evolutions and rotating frames. See [homework1_part2.ipynb](./HMW1%20p2/homework1_part2.ipynb).
- HMW2: Harmonic‑oscillator ψn, normalization/overlaps, and mp4 animations. See [homework2.ipynb](./HMW2/homework2.ipynb).
- HMW3: Qiskit PauliVec plots for |+−⟩ and Bell states; 2‑qubit Hamiltonian analysis. See [homework3.ipynb](./HMW3/homework3.ipynb).