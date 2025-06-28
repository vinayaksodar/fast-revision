# Lecture One

## Charge Generation

- Positive and negative charge generation demonstrated by:
  - Rubbing **glass with silk** (produces positive charge on glass).
  - Rubbing **rubber with cat fur**, etc. (produces negative charge on rubber).

## Charge Induction

![charge-induction](/public/images/charge-induction.png)

- **In Conductors:**
  - Free electrons move towards the charged object.
  - This movement causes **attraction** between the charged object and the conductor.

- **In Non-Conductors (Insulators):**
  - **Polarization** occurs, causing:
    - Positive charge on one side.
    - Negative charge on the other.
  - This results in **attraction** to the charged object as well.

### Example

- Rub a **balloon** on your shirt to charge it.
- Stick it on any **non-conductive** surface like a **board** or the **ceiling**.

## Electroscope Demonstration

- An **electroscope** is demonstrated.
- When a charged object touches or comes close to the electroscope, the **leaves or foils** inside it acquire like charges.
- Since **like charges repel**, the leaves **repel each other** and move apart.
- This indicates the presence of electric charge.

## Additional Note

- Every **insulator** is a **dielectric**, although it may be a **poor dielectric**.
- Walter Lewin trys to touch the rubber baloon to take the charge off but is unsuccessfull as it is an insulator. The below might be an intuitive way to think about it, confirm in future.

![charge transfer when touching insulators](/public/images/charge-transfer-insulator.png)

## Electric Force Between Two Charges

The electric force between two point charges is given by **Coulomb's Law**:

$$
F = k \frac{{|q_1 q_2|}}{{r^2}}
$$

Where:

- $F$ = electric force between the charges (in newtons, N)
- $k$ = Coulomb’s constant $(8.988 \times 10^9 \, \text{Nm}^2/\text{C}^2$
- $q_1, q_2$ = magnitudes of the two charges (in coulombs, C)
- $r$ = distance between the charges (in meters, m)
  
**Important:** This is force between two static charges, when the charges are moving there is an additional magnetic field and force due to it.

# Lecture 2

- **Introduction to Electric Fields**
  - Concept and definition of the electric field
    $$ E= \frac{F}{q} $$
  - Visualization of electric field lines

- **Formation of a Dipole by Charge Induction**
  - Demonstration using two connected metal spheres
  - Induced charges create a temporary dipole
  - Spheres are then separated to form a **permanent dipole**

- **Dipole Behavior in an Electric Field**
  - The dipole naturally aligns with the direction of the electric field

- **Visualization of Electric Field Lines**
  - Grass seeds are used to represent field lines
  - Seeds behave like tiny dipoles
  - They align themselves with the electric field, revealing its pattern

## Lec 3: Gauss's Law

This lecture introduces **Gauss's Law**, a fundamental concept in electromagnetism. While a formal proof is not provided, its utility is emphasized.

Gauss's Law is primarily used to **calculate the electric field ($\vec{E}$)** in situations with a high degree of symmetry, often without resorting to the more complex Coulomb's Law. It is most effective when such symmetry (spherical, cylindrical, planar) is present.

The integral form of Gauss's Law is:

$$\oint_S \vec{E} \cdot d\vec{A} = \frac{Q_{enc}}{\epsilon_0}$$

Where:

- $\oint_S$ represents the integral over a closed surface (known as a Gaussian surface).
- $\vec{E}$ is the electric field.
- $d\vec{A}$ is an infinitesimal area vector on the Gaussian surface, pointing outward.
- $Q_{enc}$ is the total electric charge enclosed by the Gaussian surface.
- $\epsilon_0$ is the permittivity of free space (a constant).

---

### Demonstration Insights

Key points to remember from the demonstrations:

- **Charging by Induction with Insulators:** Insulators, like glass, do not transfer charge instantaneously. When a charged insulator is brought near a metal plate, it **induces** a separation of charge within the metal. In Professor Walter Lewin's demonstration, he then touches the metal plate. This allows the like charges (those repelled by the charged insulator) to flow to the ground (his body acting as a ground). Consequently, the metal plate is left with a net charge opposite to that of the inducing object.(see image below for more clariication) [charging-via-grounding](#lec-5)

- **Balloon and Charged Plates:** In the demonstration where a balloon oscillates between positively and negatively charged plates:
  - When the balloon touches the positively charged plate, it acquires a small amount of positive charge.
  - Being positively charged, it is then attracted to the negatively charged plate.
  - Upon contact with the negative plate, it transfers the positive charge (neutralizing some negative charge) and picks up a small amount of negative charge.
  - Now negatively charged, it is repelled by the negative plate and attracted back to the positive plate.
  - This continuous back-and-forth motion of the balloon effectively transfers charge between the plates, gradually discharging them. This is why Professor Lewin needs to keep recharging the plates during the demonstration.

## Lec 4

### Key Concepts

- **Potential Energy & Electric Potential:** When calculating electric potential energy, we often consider the work done by an external force equal and opposite to the electric force ($F_{ext} = -F_E$) to move a charge from infinity to a point without changing its kinetic energy. This focuses the calculation on the change in potential energy, which defines the electric potential.
  $$ Energy (U) = \int_{\infin}^{r}F\cdot dr$$
- **Electric Potential ($V$):** A scalar quantity representing the electric potential energy per unit charge.
  $$ Potential(V) = \int_{\infin}^{r}E\cdot dr$$
  - Energy is defined for the system it has only one value potential is a field defined for every point in space.
  - It's often easier to work with potential than with electric fields, especially for complex field configurations.
  - If only concerned with changes in kinetic energy, the difference in electric potential between two points is sufficient: $\Delta K = -q \Delta V$.
- **Zero Electric Field vs. Zero Potential:**
  - If the electric field ($\vec{E}$) is zero in a region, it means the electric potential ($V$) is **constant** in that region, not necessarily zero.
- **Reference Point for Potential:**
  - The potential at infinity is conventionally taken as zero ($V_\infty = 0$).
  - For many practical applications, the Earth is also considered to be at zero potential. This is a reasonable approximation because there's a negligible net electric field between the Earth's surface and infinity, implying no significant potential difference.

## Lec 5

### Key Concepts

- **Relationship between Electric Field ($\vec{E}$) and Potential ($V$):**
  - The electric field is the negative gradient of the electric potential:
        $$\vec{E} = -\nabla V$$
        (This is often written as $\vec{E} = -\text{grad } V$)
  - **$\vec{E}$ is perpendicular to equipotential surfaces:** An equipotential surface is a surface where the potential $V$ is constant. Since $dV = 0$ along an equipotential surface, and the change in potential is related to the electric field by $dV = -\vec{E} \cdot d\vec{r}$, it implies that $\vec{E} \cdot d\vec{r} = 0$. For a non-zero $\vec{E}$ and $d\vec{r}$ (displacement along the equipotential surface), this dot product being zero means $\vec{E}$ must be perpendicular to $d\vec{r}$, and thus perpendicular to the equipotential surface.

- **Conductors in Electrostatic Equilibrium:**
  - **Zero Electric Field Inside:** The electric field inside a conductor (solid or hollow) is zero. If it weren't, charges would move, violating the assumption of electrostatic equilibrium.
  - **Charge Resides on the Surface:** Any net charge on an isolated conductor resides entirely on its outer surface.
  - **Charge Inside a Hollow Conductor:** If a charge is placed *inside* a hollow conductor (without touching it), it will induce an equal and opposite charge on the inner surface of the conductor and an equal charge of the same sign as the enclosed charge on the outer surface.
  - The surface of a conductor will be equipotential.
  - The below **approximately**(as potential is calculated ignoring induction and assuming charges are uniformly distributed) demostrates charging of a conductor by grounding which is used by walter lewin to charge via electrophorous.
![charging-via-grounding](/public/images/charging-via-grounding.png)

- **Electrostatic Shielding (Faraday Cage):**
  - A conductive enclosure (Faraday cage) blocks external static electric fields.
  - **Demonstration Note:** In the Faraday cage demonstration, AM (lower frequency) radio waves might be effectively blocked, while higher frequency transmissions (like from a microphone if it's an FM system or a different technology) might still pass through to some extent. This is because true electromagnetic waves involve changing electric and magnetic fields, and the shielding effectiveness can depend on the frequency of the wave and the material/thickness of the cage. Pure electrostatic shielding is most effective for static or slowly varying fields.

---

## Lec 6

### Key Concepts

- **Electric Field Concentration at Sharp Points:**
  - Electric fields are strongest at sharp corners or points on a charged conductor.
  - **Proof Motivation:** Consider two spheres of different radii, $R_1$ (large) and $R_2$ (small, $R_2 < R_1$), connected by a conducting wire. They will be at the same potential ($V_1 = V_2$). Since $V = \frac{kQ}{R}$ and surface charge density $\sigma = \frac{Q}{4\pi R^2}$, we can show that $\sigma_2 = \sigma_1 \frac{R_1}{R_2}$. Thus, the smaller sphere ($R_2$) will have a higher surface charge density ($\sigma_2 > \sigma_1$) and consequently a stronger electric field ($E \propto \sigma$) near its surface, even if the total charge on the larger sphere is greater.
  - **Implication:** Sparks are more likely to occur from sharp points where the electric field can exceed the breakdown strength of the surrounding medium (e.g., air).

- **Electrical Breakdown:** When the electric field in a material (like air) becomes too high, the material ionizes and becomes conductive, leading to a sudden flow of charge.

- **Types of Electrical Discharge:**
  - **Spark:** A rapid, transient discharge characterized by a single, bright channel of current.
  - **Corona Discharge:** A more continuous, less intense discharge that occurs from sharp points in high electric fields. It often appears as a faint glow and involves multiple, smaller current pathways rather than a single distinct spark.
  - **Arc Discharge:** A sustained, high-current discharge producing bright light and high temperatures.

- **Frictional Charging and Grounding:**
  - Friction can cause objects to accumulate static charge.
  - **Safety:** In environments where sparks can be dangerous (e.g., refueling stations), it's crucial to ground objects to prevent charge buildup and potential ignition. For example, gasoline nozzles are grounded because friction between the flowing gasoline and the nozzle can charge the nozzle tip, potentially creating a spark.

### **Lec 7: Energy in Electric Fields & Capacitance**

- **Energy in an Electric Field:** The energy stored per unit volume in any electric field is given by:
    $$U_E = \frac{1}{2} \epsilon_0 E^2$$
    We derive the above from a capacitor however a general proof is not given.  
    The above also means:
    $$U = \frac{1}{2}QV$$

- **Capacitance ($C$):** Initially defined as the ratio of charge to potential ($C = Q/V$) for any object. The definition is refined for a **capacitor**, which consists of two conductors. Capacitance is defined for this pair of objects, holding equal and opposite charges ($+Q$ and $-Q$). This is because capacitance fundamentally describes the ability of a system of two conductors to store energy in the electric field between them.

- **Practical Capacitors:** A real capacitor is often made of long conductive plates rolled into a compact cylinder with an insulating material (a dielectric) in between.

- **Capacitor Applications:** Capacitors are used for applications requiring a rapid release of energy, like a camera flash. A battery releases energy slowly (low current), whereas a capacitor can be charged over time and then discharged very quickly, producing a massive burst of current for a short duration.

### **Lec 8: Dielectrics**

- **Dielectrics:** Insulating materials where the molecules form small electric dipoles that align themselves with an external electric field. This alignment creates an internal electric field that opposes the external field.

- **Effect on Electric Field:** When a dielectric is inserted into a capacitor, it reduces the net electric field between the plates. The magnitude of this reduction is given by the **dielectric constant**, $\kappa$ (kappa):
    $$E_{net} = \frac{E_{original}}{\kappa}$$

- **Good Dielectrics:** Materials with molecules that are natural dipoles (polar molecules) make excellent dielectrics. Water, for example, is a very effective dielectric with a high dielectric constant ($\kappa \approx 80$). But we don't use water in capacitors as it has a very low breakdown voltage.

### **Lec 9 & 10: Electric Circuits**

- These lectures cover the fundamentals of analyzing electric circuits using **Kirchhoff's Laws** (Kirchhoff's Current Law and Kirchhoff's Voltage Law).

### **Lec 11: Magnetic Force**

- **Source of Magnetic Field:** Unlike electric fields which originate from charges, magnetic fields are created by **moving charges** (currents). There are no known **magnetic monopoles** (isolated north or south poles).

- **Force on a Moving Charge:** Because there are no magnetic monopoles, the magnetic force isn't defined for a stationary "magnetic charge." Instead, it's defined by the force it exerts on a moving electric charge:
    $$\vec{F} = q(\vec{v} \times \vec{B})$$
    This is the magnetic part of the **Lorentz Force**.
    The total electromagnetic force on a charge is:
    $$\vec{F}_{total} = q\vec{E} + q(\vec{v} \times \vec{B})$$

- **Magnetic Force Does No Work:** The magnetic force is always perpendicular to the velocity of the particle ($\vec{F} \perp \vec{v}$). Therefore, it can **never do work** on the particle or change its kinetic energy. It can only change the particle's direction.

- **Force on a Current-Carrying Wire:** The collective force on all the moving charges in a wire results in a macroscopic force on the wire itself:
    $$\vec{F} = I \int d\vec{l} \times \vec{B}$$
    Where $I$ is the current and $d\vec{l}$ is a vector representing a small segment of the wire. This principle is the basis for how electric motors work, by creating torque on a current loop in a magnetic field.  
    Note: Similar to force experienced by a charge in an electric field $F_{el} = \int Edq\hat{r}$

- **Conductors and Magnetic Fields:** Unlike conductors that block static electric fields (Faraday cage), conductors generally do not block or shield static magnetic fields.

### **Lec 13: Cyclotron**

- This lecture demonstrates the working principle of a **cyclotron**, a particle accelerator that uses a magnetic field to bend charged particles into a circular path and an electric field to accelerate them. No new fundamental formulas are introduced; it's an application of the Lorentz force.

### **Lec 14: The Biot-Savart Law**

- **Calculating the Magnetic Field:** This lecture addresses how to calculate the magnetic field produced by a current. Till now we only saw the force exerted on a currrent carrying conductor in an external magnetic field. Now we see the magnetic field it itself produces.
- The **Biot-Savart Law** gives the differential magnetic field ($d\vec{B}$) created by a small segment of a current-carrying wire ($d\vec{l}$).

- **The Formula:**
    $$d\vec{B} = \frac{\mu_0}{4\pi} \frac{I(d\vec{l} \times \hat{r})}{r^2}$$
    Where:
  - $\mu_0$ is the permeability of free space (a constant).
  - $I$ is the current.
  - $d\vec{l}$ is a vector for an infinitesimal length of the wire in the direction of the current.
  - $r$ is the distance from the wire segment to the point of interest.
  - $\hat{r}$ is the unit vector pointing from the wire segment to the point.

- **Comparison to E-Field:** This law is analogous to the formula for the electric field from a point charge ($d\vec{E} = \frac{1}{4\pi\epsilon_0} \frac{dq}{r^2}\hat{r}$). The "source element" is $I d\vec{l}$ instead of a charge $q$, reflecting the absence of magnetic monopoles. The cross product gives the magnetic field a perpendicular direction that wraps around the current-carrying wire.

Here are your refined lecture notes in a concise markdown format.

### **Lec 15: Ampere's Law**

**Ampere's Law** provides a powerful and convenient method for calculating the magnetic field ($\vec{B}$) in situations with high symmetry, much like Gauss's Law simplifies electric field calculations. Instead of integrating using the more complex Biot-Savart Law, Ampere's Law relates the magnetic field circulating around a closed loop to the total current passing through that loop.

The law is stated as:

$$\oint \vec{B} \cdot d\vec{l} = \mu_0 I_{enc}$$

- **$\oint \vec{B} \cdot d\vec{l}$** is the line integral of the magnetic field around a closed path (an "Amperian loop").
- **$\mu_0$** is the permeability of free space.
- **$I_{enc}$** is the total electric current enclosed by the path.

---

### **Lec 16: Faraday's Law & Lenz's Law**

**Lenz's Law** is a qualitative rule that describes the direction of an induced current. It states that an induced electromotive force (EMF or voltage) and the resulting current will always be in a direction that **opposes the change in magnetic flux** that created it.

This concept is mathematically described by **Faraday's Law of Induction**, which shows that a changing magnetic flux through a loop induces an EMF:

$$\oint \vec{E} \cdot d\vec{l} = -\frac{d\Phi_B}{dt}$$

- The left side, **$\oint \vec{E} \cdot d\vec{l}$**, represents the induced EMF (voltage) in a closed loop.
- The right side, **$-\frac{d\Phi_B}{dt}$**, is the negative rate of change of magnetic flux ($\Phi_B$) through the surface enclosed by the loop. The minus sign is the mathematical representation of Lenz's Law.

A crucial consequence of this is that the electric field is **no longer conservative** in the presence of a changing magnetic field. A conservative field (like the electrostatic field) has a line integral of zero around any closed path ($\oint \vec{E} \cdot d\vec{l} = 0$). Since the integral is now non-zero, the "voltage" measured between two points can depend on the path taken, which is very nonintuitive as a voltmeter connected between the same two points can measure different voltages as demonstrated in the lecture.

### Lec 17: Eddy currents

Any system will fight change so eddy currents are introduced in the material. This has application in magnetic braking, levitation etc.

### Lec 18: Displacement current

If you look at the below figure amphere's law falls apart if we take a surface as shown

![displacement-current](/public/images/displacement-current.png)

So maxwell thought if there a changing magnetic field produced an electric field maybe a changing electric field produces a magnetic field and amended ampheres law.

$$\oint \vec{B} \cdot d\vec{l} = \mu_0 (I_{enc} + \epsilon\frac{d\phi_e}{dt})$$

### Lec 19: Self Inductance

The **inductance ($L$)** of a component is defined by the relationship between the magnetic flux ($\Phi_B$) it produces and the current ($I$) flowing through it.

**Definition of Inductance:**
The magnetic flux is directly proportional to the current.
$$\Phi_B = L I$$
This is analogous to the definition of capacitance: $Q = CV$.

---

**Self-Induced EMF (Voltage):**
According to Faraday's Law, a change in magnetic flux induces an electromotive force (EMF) or voltage ($\mathcal{E}$). The induced EMF in an inductor is:
$$\mathcal{E} = -L \frac{dI}{dt}$$
The negative sign (from Lenz's Law) indicates that the induced EMF opposes the change in current. This is the mathematical reason why inductors "fight" changes in current. This is analogous to how capacitors "fight" sudden changes in voltage: $I = C \frac{dV}{dt}$.

---

**Energy Stored in an Inductor:**
The energy ($U_L$) stored in the inductor's magnetic field is given by:
$$U_L = \frac{1}{2}LI^2$$
This is analogous to the energy stored in a capacitor's electric field: $U_C = \frac{1}{2}CV^2$.

---
We see that current is lagging behind voltage when we analyse AC circuits with an inductor.
We see two applications of this one in levitation to make the current in the upper coil opposite to the current induced i.e eddy current which also has some inductance associated with it.
The other to damp higher frequencies when we are recieving a current signal that is being used to play music
Yoou can analyse AC circuits using the standard partial derivatives or the complex way but the complex impedance is only valid for sinusoidal signals although you can break any signal into sines and cosines using fourier and use this method.

### Lec 19: dia para ferromagnetic materials
Don't try to compare to dielectric. In that field reduces and it is attracted.
Diamagnetic - Field inside it reduces but it is repelled in a non uniform magnetic field.
Paramagnetic - Field inside it increases i.e magnetic dipoles align in the direction of magnetic field for some reason only explained with quantum mechanics. It is attracted in a non uniform magnetic field
Ferromagnetic - Field inside it increases strongly it is also attracted strongly.