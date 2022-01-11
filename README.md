# Vaja3-ADC-trigger-timer-conversion-STM32F0

Vprašanja:

Na zaslonu se vam mora usterzno pobarvati izbrani pin v zeleno barvo. Kaj se izpiše poleg pina? Pin PC0, zraven se izpiše ADC_IN10
Aktiviramo zeleno LED diodo na izhodu PD12
V Clock Configuration spremenimo APB1 Timer clock (MHz) na 16 MHz. Kaj opazimo? Ta frekvenca se spremeni in prilagodi še nekatere 
druge frekvence.
V razdelku TIM1, pod Counter Settings, bi radi časovniku spremenili frekvenco na 1 kHz, zato moramo frekvenco ABP1 Timer Clock preskalirati v polju Prescaler (PSC – 16 bit value). Koliko znaša ta vrednost? Ta vrednost znaša 16.000.

Komentar:

Ko sva prvič poskusila naložiti program na ploščico, sva imela problem pri nalaganju (GDB napaka), ampak sva ga hitro rešila, ker
sva imela isti problem pri vaji 1. Na TIM1 se ni dalo nastaviti na Timer 1 Trigger Out even, zato sva namesto TIM1 izbrala TIM2. 
Pri programiranju sva imela porblem, ker nama adcVal v Live expressions ni prkazoval vrednosti. Problem sva rešila, da sva adcVal 
prestavila v While, nato nama je delovalo brez težav. 

