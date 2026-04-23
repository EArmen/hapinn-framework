# Supplementary Note: Toy Model Derivation

This note records the derivation of the one-mode analytical toy model used in the manuscript.

## Model problem

Consider the one-dimensional boundary-value problem

\[
-u''(x;\mu)=\mu \pi^2 \sin(\pi x), \qquad x\in(0,1), \qquad u(0;\mu)=u(1;\mu)=0.
\]

Its exact solution is

\[
u^\star(x;\mu)=\mu \sin(\pi x).
\]

## One-mode surrogate

We restrict the surrogate to the one-mode ansatz

\[
u_\alpha(x;\mu)=\alpha(\mu)\sin(\pi x).
\]

Let the anchor solver produce

\[
u_h(x;\mu)=a_h(\mu)\sin(\pi x).
\]

## Residual term

Since

\[
-u_\alpha''(x;\mu)=\alpha(\mu)\pi^2\sin(\pi x),
\]

the residual is

\[
-u_\alpha''(x;\mu)-\mu\pi^2\sin(\pi x)=\pi^2(\alpha(\mu)-\mu)\sin(\pi x).
\]

Therefore,

\[
\int_0^1 \left|-u_\alpha''(x;\mu)-\mu\pi^2\sin(\pi x)\right|^2 dx
=
\pi^4(\alpha(\mu)-\mu)^2 \int_0^1 \sin^2(\pi x)\,dx.
\]

Using

\[
\int_0^1 \sin^2(\pi x)\,dx=\frac12,
\]

we obtain

\[
\int_0^1 \left|-u_\alpha''(x;\mu)-\mu\pi^2\sin(\pi x)\right|^2 dx
=
\frac{\pi^4}{2}(\alpha(\mu)-\mu)^2.
\]

## Toy loss

The toy HAPINN loss becomes

\[
\mathcal{J}_{\mathrm{toy}}(\alpha)=
\frac{\lambda_r\pi^4}{2}|\alpha(\mu)-\mu|^2
+
\lambda_a|\alpha(\mu)-a_h(\mu)|^2.
\]

This closed-form model shows explicitly how the anchor weight and residual weight interact.
