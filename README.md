# Concentração em Sistemas de Tanques

O sistema de equações acoplados pode ser visto conforme:

\[
\begin{aligned}
V_1 \frac{dc_1}{dt} &= Q_{01} c_{01} + Q_{31} c_3
                      - (Q_{12} + Q_{15}) c_1 \\[6pt]

V_2 \frac{dc_2}{dt} &= Q_{12} c_1
                      - (Q_{23} + Q_{24} + Q_{25}) c_2 \\[6pt]

V_3 \frac{dc_3}{dt} &= Q_{03} c_{03} + Q_{23} c_2
                      - (Q_{31} + Q_{34}) c_3 \\[6pt]

V_4 \frac{dc_4}{dt} &= Q_{24} c_2 + Q_{34} c_3 + Q_{54} c_5
                      - Q_{44} c_4 \\[6pt]

V_5 \frac{dc_5}{dt} &= Q_{15} c_1 + Q_{25} c_2
                      - (Q_{54} + Q_{55}) c_5
\end{aligned}
\]

Para aplicar o sistema de resuloção de EDO's de RK4, aplica-se a teoria de espaços de estados.
Criando assim dois vetores, um termo das coordenadas generalizadas e outro de suas derivadas.
No código a função irá calcular o vetor das derivadas, e substitui-los no RK4
