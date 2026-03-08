# Telecommunications Traffic Calculator: Erlang & Engset Models

A Python-based desktop application for solving queuing theory and network optimization problems. The tool provides a graphical interface to calculate key parameters of telecommunications traffic using two fundamental teletraffic models: the Erlang B formula (infinite sources) and the Engset formula (finite sources).

### Erlang Model (Erlang B)
Used for systems where the number of potential users (traffic sources) is assumed to be infinite. The application allows you to calculate one of the following parameters when the other two are known:
* **A (Traffic Intensity in Erlangs):** Total traffic offered to the system.
* **B (Blocking Probability):** The probability that a call/request is rejected due to all channels being busy.
* **N (Number of Channels):** The number of available resources/lines needed to meet a specific blocking probability.

### Engset Model
Used for systems with a strictly limited (finite) number of users or traffic sources (e.g., local networks, military communication systems). Unlike Erlang, it requires an additional parameter:
* **Number of Sources (Users):** The total finite population generating traffic.
* Calculates **A, B, or N** while accounting for the fact that a user currently being served cannot generate new requests.

## Functionalities

* **Bidirectional Solvers:** The user can select which variable to solve for (A, B, or N). The GUI automatically disables the corresponding input field.
* **Data Visualization:** Uses `matplotlib` to plot dependencies between parameters (e.g., how Number of Channels (N) affects Blocking Probability (B) under a constant Traffic Intensity). 
* **Input Constraints:** Implements `QRegularExpressionValidator` to ensure inputs fall within mathematically valid bounds for Erlang/Engset models (e.g., B must be between 0.001 and 0.999).
* **Result Logging:** A separate `QTextEdit` window records a history of all calculations performed during the session.
* **Theory Reference:** Built-in HTML-formatted theory tabs explaining the formulas and real-world use cases of both models.



## Screenshots

*Main Interface*
![Main Interface](https://github.com/Asteria04/Traffic-calculator-Erlang-Engset/blob/main/Zrzut%20ekranu%202026-03-08%20220702.png)

*Calculator Dashboard *
![Analytical Dashboard](https://github.com/Asteria04/Traffic-calculator-Erlang-Engset/blob/main/Zrzut%20ekranu%202026-03-08%20215826.png)
