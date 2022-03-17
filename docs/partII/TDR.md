# Time-domain reflectometry

![](TDR/header.jpg){: .center}

The properties of waveforms travelling through cables with different characteristic impedances are investigated. The behaviour of reflected waves from boundaries of high, low, and matched impedance is observed and related to the wave equation, and the characteristic impedance and speed of pulses in a cable are used to compare the cable inductance and capacitance to theoretically calculated values.

---

## Introduction

\subsubsection*{Objectives}

\begin{enumerate}
\item To observe and record the waveforms associated with reflections off of barriers with varying characteristic impedances.

\item To study the effect of matched impedance on pulse reflections.

\item To compare the characteristic inductance and capacitance of the cables derived from measurements of the pulse speed and impedance to the theoretically predicted values.
\end{enumerate}

\subsubsection*{Equipment}

Signal generator, oscilloscope (digital or analogue), potentiometer (three-terminal voltage divider), coaxial cable, twisted pair wire, multimeter, and leads with connectors to allow for short and open circuit terminations.  The lengths of the cables is written on the cable spools (between 40 and $\approx$300~m) and may be assumed to be accurate to $\pm$0.1~m; the characteristic impedance of the coaxial cable can be obtained from the cable specifications, and the impedances of the oscilloscope and signal generator will be found on the equipment or in the relevant manuals.

\subsubsection*{Principal Data Taken}

\begin{enumerate}
\item Graph or photograph of the incident and any reflected pulses for both the short circuit and open circuit cases, for the coaxial cable and the twisted pair wire.

\item Velocity of the pulses in both test cables.

\item Characteristic impedance Z$_0$ of the twisted pair wire and coaxial cable.
\end{enumerate}

\subsubsection*{Things to Watch Out For}

\begin{itemize}
\item The TDR setups on different benches have slightly different coaxial cables and twisted pair test wires, which may have very different characteristic impedances, lengths, and physical constructions (e.g., a single pair of conductors vs.\ a double pair in parallel). Make sure you include the labels of the cables used in your report. {\em Check with your demonstrator to see if the cables you are using have the properties you think they do!}

\item There may be multiple reflected pulses in the system, some with very low amplitudes; search the oscilloscope trace carefully and relate observed features to physical boundaries in the system to make sure you understand the paths the signal may be taking.
\end{itemize}

\subsection{Theoretical Background}

An electromagnetic signal in a wire is a form of wave, with its propagation speed and dispersive properties determined by the medium in which the wave travels. For a wire, these properties are typically summarised by a few related measurable properties: the characteristic impedance Z$_0$, the inductance per unit length (L$^{\prime}$) and the capacitance per unit length (C$^{\prime}$); these are determined by the geometry and dielectric properties of the wire and any associated shielding.

In general when a signal crosses from one wire to another, or encounters a junction, device, or break in the wire, a reflected pulse is generated because the signal "sees" the change in medium as an increase or decrease in Z$_0$. In the ideal case, when no energy is lost to dissipative effects, the expression relating the incident and reflected pulse voltage is

\[ \label{eqn:vrefl}
\frac{V_r}{V_i} = \frac{Z_L - Z_0}{Z_L + Z_0},
\]

where V$_i$ and V$_r$ are the incident and reflected voltages respectively, and Z$_L$ is the load impedance (impedance of the barrier, device or new wire). Clearly the voltage of the reflected pulse can be very high, near zero, or even negative, depending on the relationship between Z$_0$ and Z$_L$.  Equation~\ref{eqn:vrefl} can be transformed into the equivalent equation for the current using Ohm's law. Similar expressions can be obtained for any wave, for example acoustic waves in the Earth encountering different rock layers, or ocean waves travelling across the boundary of the continental shelf.

A transmission line with two conductors like a coaxial or twisted pair cable can be modelled in circuit theory as a long "ladder" formed by two wires with some series inductive impedance per unit length along the two wires and some parallel capacitive impedance per unit length across the "rungs" of the ladder. This formulation leads to a description of the change in voltage and current with distance along the transmission line ($dV/dx$ and $dI/dx$), the solution of which yields a wave equation in V (and in I).

For a single wave solution in one direction, the solution of the wave equation with the characteristic impedance Z$_0$ eventually gives:

\[ \label{eqn:zchar}
Z_0 = \frac{V}{I} = \sqrt{\frac{L^{\prime}}{C^{\prime}}}.
\]

In a lossless transmission line whose length is much shorter than the wavelength of the signal, the inductance per unit length L$^{\prime}$ can be determined from the definition of inductive reactance and the relationship between frequency, wavelength and wave velocity $v$.  The complete derivation is given in Terman (1955, Ch.\ 4).  For the purposes of this lab, the result of greatest interest is:

\[ \label{eqn:lchar}
L^{\prime} = \frac{Z_0}{v}
\]

Equations~\ref{eqn:zchar} and \ref{eqn:lchar} can be combined to derive a similar expression relating C$^{\prime}$ to $v$ and Z$_0$.  Using these equations allows the derivation of C$^{\prime}$ and L$^{\prime}$ from measurements of the pulse $v$ and Z$_0$.

C$^{\prime}$ and L$^{\prime}$ are ultimately determined by the construction of the transmission line. A coaxial cable consists a solid conducting cylinder separated from a hollow cylindrical conductor by a dielectric material as shown in Figure~\ref{fig:coaxial}.  For inner and outer radii $a$ and $b$ respectively, the properties of the cable are given by:

\begin{eqnarray} \label{eqn:coaxial}
C^{\prime} & = & \frac{2\pi\kappa\epsilon_0}{\ln\left(b/a\right)} \\
L^{\prime} & = & \frac{\mu_0}{2\pi}\ln\left(b/a\right)
\end{eqnarray}

where $\kappa$ is the dielectric constant of the insulator and $\epsilon_0$ and $\mu_0$ are
the permittivity and permeability of free space, with their usual values.

Because the twisted-pair wire has a different geometry, the transmission properties are quite different, and
are given by

\begin{eqnarray}
\label{eqn:twisted1}
C^{\prime} & = & \frac{\pi\kappa\epsilon_0}{\cosh^{-1}\left(s/2r\right)} \\
L^{\prime} & = & \frac{\mu_0}{\pi}\cosh^{-1}\left(s/2r\right)
\label{eqn:twisted2}
\end{eqnarray}

In this case the two wires have radius $r$ and are separated by a fixed thickness $s$ of insulating material, as seen in Figure~\ref{fig:twisted}. $\cosh^{-1}$ is the inverse hyperbolic cosine function, which may not be available on a typical hand calculator but is defined in most spreadsheet programs and mathematical packages such as Mathematica or Matlab. In transmission lines comprising multiple pairs in parallel, the formula must be modified using the rules for combining impedances in parallel.  This may become important depending on which twisted-pair wire you are using\footnote{The burglar alarm wire comprises two pairs of twisted strands, which are combined in parallel by the connectors at the cable ends. In Figure~\ref{fig:twisted}, imagine a second pair oriented 90$^{\circ}$ away from from the wires shown.}.

\noindent\begin{minipage}{0.48\textwidth}
\centering
\includegraphics[width=5.0cm]{TDR/coaxial.pdf}
\captionof{figure}{Cross-section of a coaxial cable.  \label{fig:coaxial}}
\end{minipage}%
\hfill
\begin{minipage}{0.48\textwidth}
\centering
\includegraphics[width=5.0cm]{TDR/twisted.pdf}
\captionof{figure}{Cross-section of a twisted-pair wire (single pair). \label{fig:twisted}}
\end{minipage}%

\subsection{Procedure}

Start by connecting the signal generator to the oscilloscope through the T-junction. You will test two types of transmission lines by connecting them to the other side of the T-junction: first a twisted-pair wire (at one of the benches this is a telephone wire, and on the other it is a burglar alarm wire), and then a coaxial cable . Both the coaxial and twisted-pair lines have been prepared with connectors on the end so that you can easily use them in the short circuit (low terminating impedance) and open circuit (high terminating impedance) conditions.

Set the signal generator to a single pulse of narrow width. The required cycle time will depend on the cable length. Set up the signal generator and the oscilloscope so that you can see just a few of the pulses on the screen. The first of these will be the generated pulse. When you have the time baseline correctly adjusted, the other pulses will be reflected ones. Ask your demonstrator for assistance if you are having trouble setting up the apparatus or observing the pulses.

\begin{enumerate}
\item Examine the waveforms on the twisted-pair line in both the short circuit (ends of the leads connected) and open circuit (ends disconnected) conditions. Try to associate each feature in the diagram with a physical interaction between the pulse and a component of the apparatus. Sketch or photograph the pulses and label them accordingly. In some cases there may be multiple pulses observed; search carefully for low-amplitude features, and think carefully about their origin. Note that the $x$-axis of your graph should have the coordinates of time (microseconds $\mu$s or nanoseconds ns). In your report, explain qualitatively why the series of pulses decreases in amplitude, as well as the reason for the polarity of every pulse observed.

\item Calculate the speed of the pulses along the line by comparing the time coordinates of the initial and reflected pulses. Express this answer both in m~s$^{-1}$ and as a fraction of the speed of light. Think carefully about the sources of uncertainty that creep into your result, and include these factors in your reported error.

\item Connect the potentiometer to the end of the wire to use it as a variable impedance termination. Find the characteristic impedance Z$_0$ of the twisted-pair wire in accordance with Equation~\ref{eqn:vrefl} as follows: change Z$_L$ by turning the dial on the potentiometer. When the amplitude of the reflected pulse drops to zero, the impedance of the potentiometer is matched to the line impedance. Z$_L$ can be measured with a multimeter.  In your report, explain carefully how you determined the condition of minimal reflection and how you determined the uncertainty in your estimate of Z$_0$.

\item Repeat the experiment using the coaxial cable (omitting the determination of Z$_0$ since the coaxial cable is well-standardised at Z$_0$ = 50~$\Omega$). Describe any differences in the oscilloscope trace between the twisted-pair and the coaxial cases, and account for them referring to Equation~\ref{eqn:vrefl} and the impedances of the signal generator and oscilloscope.
\end{enumerate}

\subsection{Calculations}

You have experimentally measured the pulse velocity $v$ and the characteristic impedance Z$_0$ for two types of transmission line.  With these data you can calculate the inductance and capacitance per unit length of the lines, and compare those to the theoretical predictions for the two types of line. In this experiment, the length of the transmission line is known and the reflectometry is used to determine the pulse velocity, but in a real field situation we may have the opposite case, in which the velocity is known.  In this case the pulse timing can tell you the distance between the signal generator and a change in impedance such as a break in the line (as well as the nature of the break in the line).

Do the following calculations for both cables tested:

\begin{enumerate}
\item Use $v$ and Z$_0$ to find L$^{\prime}$ and C$^{\prime}$ for the transmission line (Equations~\ref{eqn:zchar} and \ref{eqn:lchar}). It may be useful to remember that the units for L$^{\prime}$ and C$^{\prime}$ are henries per metre (H$\cdot$m$^{-1}$) and farads per metre (F$\cdot$m$^{-1}$), respectively.  The SI unit prefixes for 10$^{-12}$, 10$^{-9}$, and 10$^{-6}$ are pico-, nano-, and micro-, respectively.

\item Using the cable specifications, look up the characteristic impedence of the coaxial cable. Does the value agree with your measurement? Consider the formulae for theoretical calculation of L$^{\prime}$ and C$^{\prime}$ (Equations~\ref{eqn:coaxial}--\ref{eqn:twisted2}). Using the appropriate values for the two wires, find the expected L$^{\prime}$ and C$^{\prime}$ of both transmission lines. Do your empirically determined values agree with the theory?  If not, discuss some possible reasons for the disagreement.  The transmission line properties for some of the cables are as follows. {\bf Don't forget to specify in the report labels of the cables used.}

\begin{itemize}
\item {\bf Coaxial cable:} $\kappa$ = 2.3$\pm$0.1(high-density polyethylene); inner diameter $a$ = 0.90 $\pm$0.05~mm;  outer diameter $b$ = 3.80 $\pm$0.05~mm.

\item {\bf Telephone wire:} $\kappa$ = 2.3$\pm$0.1; wire diameter 2$r$ = 0.52 $\pm$0.02~mm; pair separation $s$ = 0.90 $\pm$0.05~mm.

\item {\bf Burglar alarm wire:} $\kappa$ = 4.3$\pm$0.1 (PVC); wire diameter 2$r$ = 0.54 $\pm$0.02~mm; pair separation $s$ = 1.05$\pm$0.05~mm; Note in your calculations that there are two pairs of cables, connected in parallel.

\end{itemize}
\end{enumerate}

\subsection{Bonus Section}

For a couple of extra marks, derive Equations~\ref{eqn:twisted1} and \ref{eqn:twisted2} using the definitions of capacitance and inductance together with the geometry in Figure~\ref{fig:twisted}.
\vspace{18pt}

\noindent{\bf References}\\
\noindent Dickey, J. 2018, {\it Lecture Notes for KYA211/374}, available on MyLO\\
\noindent Pain, H.J. 2005, {\it The Physics of Vibrations and Waves, 6th Ed.}, (Wiley: London)\\
\noindent Terman, F. 1955, {\it Electronic and Radio Engineering, 4th Ed.}, (McGraw-Hill: New York)

[^1]: N. A. me, _Title_, (Publisher, location, year) [page]

--8<-- "includes/abbreviations.md"
