# Quantum Computing N-Queens Solver
 1. Problem Description <br />
    N-Queens is a problemm of placing N number of queens on a NxN chessboard that no queens can attack each other. In other words, each row and column will have only one queens and no more than one queens will be an diagonal line. <br />
 2. Initialization <br />
    Each qubits will represent squares on chessboard. Unlike standard procedure to use Hadamard gates to set all qubits in uniform superposition, we will set n numbers of n set of qubits into superposition - set of qubits each represents row and each states represents one queen in one position. <br />
    |W⟩=1/√𝑛(|10∙∙∙0⟩+|01∙∙∙0⟩+|00∙∙∙1⟩) <br />
    |𝜓⟩=|W⟩_1⊗|W⟩_2⊗⋯⊗|W⟩_𝑁 <br />
 4. Oracle <br />
    We can represent classical logic gates - NOT, XOR, AND - with X, CNOT, and AND gates respectively. Condition for rows was already met during initialization, so column and diagonal conditions are represented in quantum circuit by transforming boolean conditions into quantum gates. <br />
 5. Amplification <br />
    Amplification is performed by using conjugate transpose of operator W we used on initialization step. <br />
 6. Number of grover operation <br />
    N-Queens problem has multiple solutions. Equation for number of Grover Operation for multi-solution search problem is <br />
    𝜃=〖sin^(−1) (√(𝑆/𝑁^𝑁 )) <br />
    𝑡=|𝜋/4𝜃|=|𝜋/4𝜃 √(𝑁^𝑁/𝑆)| <br />
    where number of states is 𝑁^𝑁 and number of solutions is 𝑆.
    For example, when N=8 and S=92, t=335.
