# BD-P3-CASO-3
1*) σ rol='programador' ∧ codp='P22-11' ∧ cantHoras > 10 TRAB
2*) REVISAR PORQUE NO SE SI EL NATURAL JOIN ES CON EMPLEADOS O TRAB*) EMPLEADOS ⨝ ((π cuil σ rol='analista' ∧ year(fDesde) ≤ 2023 ∧ year(fHasta) ≥ 2023 TRAB) ∩ (π cuil σ rol='diseñador' ∧ year(fDesde) ≤ 2023 ∧ year(fHasta) ≥ 2023 TRAB))
3*) (π cuil ρ cuil ← lider PROYECTOS) - π cuil EMPLEADOS
4*) A= π codp σ cliente='OSSE' PROYECTOS
    π cuil,codp TRAB ÷ A
5*) A= π C,CP,R ρ C ← cuil,CP ← codp,R ← rol TRAB
    B= (π cuil,codp,rol TRAB) ⨯ A
    (π cuil σ cuil=C ∧ codp=CP ∧ R≠rol B) - (π cuil ρ cuil ← lider PROYECTOS)
6*) A= π C,CP,R ρ C ← cuil,CP ← codp,R ← rol TRAB
    B= (π cuil,codp,rol TRAB) ⨯ A
    (π cuil σ cuil=C ∧ codp=CP ∧ R≠rol B)
7*) A= π cuil σ codp='P22-05' ρ cuil ← lider PROYECTOS
    π cuil, nom (EMPLEADOS ⨝ (A ∪ (π cuil σ codp = 'P22-05' TRAB)))    
8*) EMPLEADOS ⨝ ((π cuil,codp σ rol='analista' ∧ year(fDesde) ≤ 2023 ∧ year(fHasta) ≥ 2023 TRAB) ∩ (π cuil,codp σ rol='diseñador' ∧ year(fDesde) ≤ 2023 ∧ year(fHasta) ≥ 2023 TRAB))
