# Forelesninger til RAD210
# 

Interaktive Quarto-forelesninger
Ivan I. Maximov

## Introduksjon

Emnet bygger MR fra bunnen: fra matematikken bak bildet, via sikkerhet, signal og
sekvenser, til de kliniske teknikkene (diffusjon, spektroskopi, fMRI, SWI) og hvordan
opptaket gjøres raskt, helt fram til dyp læring i dagens skannere. Hver forelesning har
innebygde, numerisk verifiserte apper slik at studentene kan leke med prinsippene selv.

## Modul 0 Matematisk grunnlag 

Fouriertransformasjonen som bindeledd mellom k-rom og bilde. Frekvens- og fasekoding,
sampling og Nyquist. App: bygg et bilde k-linje for k-linje og se hva hver frekvens
bidrar med.

## Modul 10 MR-sikkerhet

De tre feltene og deres farer — statisk felt (projektiler, implantater), gradienter
(nervestimulering, støy) og RF (SAR, oppvarming) — samt soner, quench og screening.
Praktisk risikoforståelse før man går inn i skannerrommet.

## Modul 3 Sekvenser

Flippvinkel og snitteseleksjon; RF-pulsformer. Spinnekko (SE) vs.
gradientekko (GRE), TR/TE og hvordan k-rom fylles for å styre kontrast. App:
RF-puls-simulator.

## Modul 5 Artefakter (del I og II)

Ni klassiske artefakter: bevegelse, aliasing, kjemisk skift, skyggelegging, RF,
susceptibilitet, gradient, Gibbs pluss k-linjefeil, delvolum og synsfelt-optimalisering. 
App: én motor som slår hver artefakt av og på.

## Modul 6 Diffusjon-MRI

Brownsk bevegelse og Einstein-relasjonen (r^2 = 2nDt); Stejskal–Tanner (PGSE), b-verdi
og S = S0 * exp(-bD); ADC, diffusjonstensoren og FA/MD/AD/RD; kryssende fibre -> DKI;
traktografi. Klinikk: hjerneslag, nevrokirurgi, hjerte, bryst, helkropp. Apper: Brownsk
bevegelse, PGSE, ADC, tensor, traktografi.

## Modul 6 MR-spektroskopi

Kjemisk skift (ppm) og metabolittene NAA, Cr, Cho, mI, Glx og laktat; J-kobling og
laktat-inversjon ved TE 135 ms; FID -> Fourier -> spektrum, vannundertrykking,
STEAM/PRESS, enkelt voksel vs. MRSI. Apper: FID->spektrum, metabolitt-spektrum,
TE/laktat, MRSI, sykdomsmønstre.

## Modul 6 Funksjonell MRI

BOLD-mekanismen (paramagnetisk deoksyhemoglobin -> mindre signal ved aktivering),
hemodynamikk-responsfunksjonen, eksperimentdesign og midling, aktiveringskart (GLM) og
funksjonell konnektivitet. Apper: BOLD, HRF, design/midling, aktivering, konnektivitet.

## Modul 6 Susceptibilitetsvektet avbildning (SWI)

Magnetisk susceptibilitet og dipolfeltet (3cos^2(theta) - 1); fase phi = -gamma*dB*TE;
SWI = magnitude * (fasemaske)^n; mIP-venografi; para- vs. diamagnetisk (blødning vs.
kalk). Klinikk: mikroblødninger, jern, venøs oksygenering. Apper: felt/fase,
SWI-pipeline, mIP, para/dia, mikroblødninger.

## Modul 9 Rask MRI

Del 1 (raske sekvenser og k-rom): skanntid = TR*N/ETL; ekkotog (TSE), gradientekko,
undersampling -> aliasing, partiell Fourier (hermitisk symmetri), EPI, spiral/
non-kartesisk + gridding.
Del 2 (parallell avbildning): spolefølsomhet og SoS, SENSE-utfolding, g-faktor
(SNR = SNR_full / (g * sqrt(R))), GRAPPA, SMS/multiband + CAIPIRINHA, pTx.
Apper med ekte FFT og lineær algebra i nettleseren.

## Modul 9 — Dyp læring for raskere MRI

Fra nevron, aktivering og gradientnedstigning til CNN og overtilpasning;
DL-rekonstruksjon (bilderom / k-rom / hybrid), utrullede fysikk-informerte nett
(VarNet/MoDL), selvveiledet læring og diffusjonsmodeller. I skannerne i dag: AIR Recon
DL, Deep Resolve, SmartSpeed, AiCE, Sonic DL — 50–60 % (opptil 86 %) kortere tid.
Apper: nettet som lærer (ekte backprop), konvolusjon, DL-vs-CS-rekonstruksjon, utrullet
nett, lært sampling. Avslutter med fallgruvene: hallusinasjon, generalisering og
validering.
