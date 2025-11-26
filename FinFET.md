### Detailed Notes on FinFET  
(Complete, Clear & Exam/Interview Ready)

#### 1. Why FinFET Was Invented?
Planar MOSFET stopped scaling properly below 22nm due to **Short Channel Effects (SCE)**:
- Severe leakage current (subthreshold leakage)
-threshold leakage)
- Drain-Induced Barrier Lowering (DIBL)
- Poor electrostatic control of channel by gate
- Threshold voltage (Vt) variation
- Very high off-state current (Ioff)

**Solution**: Give the gate **3D control** over the channel → FinFET was born.

#### 2. What is a FinFET?
- It is a **3D multi-gate transistor** built on an SOI (Silicon-On-Insulator) or bulk silicon substrate.
- The channel is a thin vertical “fin” of silicon.
- The gate wraps around the fin on **three sides** (Tri-gate (Tri-gate) → much better control than planar.
- Invented by Prof. Chenming Hu (UC Berkeley) in 1999.  
  First commercialized by Intel at **22nm in 2011** (Ivy Bridge).

#### 3. Structure of FinFET

| Part               | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| Fin                | Thin vertical silicon wall (height 30–50 nm, width 5–10 nm)                 |
| Gate               | Wraps around top + two sidewalls of the fin → 3-sided control               |
| Source/Drain       | Raised S/D (epitaxial growth) to reduce resistance                          |
| Gate Oxide         | Very thin High-k dielectric (HfO₂) + metal gate                             |
| Substrate          | Bulk or SOI (SOI reduces leakage)                                           |

#### 4. Types of FinFET
| Type               | Gates Active | Electrostatic Control | Used By          |
|--------------------|--------------|-----------------------|------------------|
| Double-Gate        | 2 sides      | Good                  | Research         |
| Tri-Gate (most common) | 3 sides   | Very good             | Intel, TSMC, Samsung |
| Gate-All-Around (GAA) | 4 sides   | Best (next-gen)       | Samsung 3nm, TSMC 2nm (nanosheet) |

#### 5. Key Parameters in FinFET

| Parameter         | Symbol   | Typical Values (5nm–3nm nodes) | Effect                                      |
|-------------------|
| Fin Height        | Hfin     | 40–55 nm                      | ↑ Hfin → ↑ drive current                    |
| Fin Width         | Wfin     | 5–8 nm                        | ↓ Wfin → better SCE control                 |
| Fin Pitch         |          | 24–42 nm                      | Determines density                          |
| Effective Width   | Weff     | = 2×Hfin + Wfin               | ~3× more than planar for same footprint     |
| Gate Length       | Lg       | 12–20 nm                      | Physical gate length                       |

#### 6. Advantages of FinFET over Planar MOSFET

| Advantage                          | Explanation                                                                 |
|------------------------------------|-----------------------------------------------------------------------------|
| Excellent Short Channel Control    | Gate controls channel from 3 sides → reduces leakage                        |
| Higher ON current (Ion)            | Larger effective width (Weff) in same area                                  |
| Lower leakage (Ioff)             | 100–1000× lower than planar at same node                                    |
| Better subthreshold swing          | ~70–80 mV/decade (vs 90–120 in planar)                                      |
| Reduced DIBL & Vt variation        | Stronger gate control                                                      |
| Scalable down to 3nm                 | Planar failed at 22nm                                                      |

#### 7. Disadvantages of FinFET

| Disadvantage                     | Reason / Effect                                                  |
|----------------------------------|------------------------------------------------------------------|
| Complex & costly fabrication     | Fin etching, high-aspect ratio, parasitic capacitance            |
| Quantized width                  | Wfin must be multiple of crystal lattice → limited drive strength choices |
| Higher parasitic capacitance     | Between gate and S/D                                             |
| Corner effects                   | Electric field concentration at fin corners                              |
| Self-heating                     | Poor heat dissipation from narrow fin                                    |
| Difficult to go below 3nm        | 3nm Fin pitch and height become too challenging → replaced by GAA       |

#### 8. FinFET vs Planar MOSFET (Comparison Table)

| Parameter                | Planar (28nm)      | FinFET (14nm/10nm)   | FinFET (5nm/3nm)    |
|--------------------------|--------------------|----------------------|---------------------|
| Gate control             | 1 side             | 3 sides              | 3 sides             |
| Drive current / area     | Lower              | ~1.7× higher         | ~2.5× higher        |
| Subthreshold swing       | ~100 mV/decade     | ~75 mV/decade        | ~70 mV/decade       |
| Ioff                     | High               | Very low             | Extremely low       |
| Scalability              | Stopped at 22nm    | Up to 5nm/3nm        | Last node ~3nm      |

#### 9. Evolution of FinFET Nodes

| Company   | Node   | Year | Fin Pitch | Notes                                      |
|-----------|--------|------|-----------|--------------------------------------------|
| Intel     | 22nm   | 2012 | 60 nm     | World’s first FinFET CPU (Ivy Bridge)      |
| Intel     | 14nm   | 2014 | 42 nm     | Broadwell                                  |
| TSMC      | 16nm   | 2015 | 48 nm     | Apple A9, Snapdragon 820                   |
| TSMC      | 7nm    | 2018 | 30 nm     | Apple A12, Kirin 980                       |
| TSMC      | 5nm    | 2020 | 28 nm     | Apple A14/M1, Snapdragon 888               |
| TSMC      | 3nm    | 2023–24| 24 nm     | Apple A17 Pro, M2 Ultra                    |

After 3nm → Industry moving to **Gate-All-Around (GAA) / Nanosheet FETs** (Samsung 3nm GAA in 2022, TSMC N2 in 2026).

#### 10. Future After FinFET
| Technology         | Description                              | When       |
|--------------------|------------------------------------------|------------|
| Nanosheet / GAAFET | Stacked horizontal nanosheets, gate on all 4 sides | 2025–2027 |
| CFET               | Complementary FET (N+P stacked vertically) | ~2028+    |
| 2D Materials       | MoS₂, WS₂ channels                       | Research   |
| Forksheet FET      | Reduced parasitics between N and P       | Research   |

#### Summary One-Liner
**FinFET saved Moore’s Law for a decade (2011–2022) by giving the gate 3D control over a vertical silicon fin, dramatically reducing leakage and allowing scaling down to 3nm.**

Best for exams/interviews:
Draw the 3D structure of Tri-gate FinFET and label: Fin, Gate, S/D, High-k dielectric, and show how Weff = 2×Hfin + Tfin.

Let me know if you want:
- Hand-drawn style FinFET diagrams explained
- Comparison with GAA/nanosheet
- FinFET layout rules
- Parasitic extraction in FinFET

Happy learning! 🚀
