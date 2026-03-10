

#### Introduction
In quantum computing, linear algebra is the mathematical foundation used to describe quantum states and the operations performed on them. The state of a quantum system is represented as a vector in a complex Hilbert space, and quantum operations—namely quantum gates—are represented by unitary matrices.

#### Qubits as Vectors
A single qubit can be represented as a two-dimensional column vector. The standard computational basis states are denoted using Dirac notation as |0⟩ and |1⟩.

|0⟩ = [1, 0]ᵀ  
|1⟩ = [0, 1]ᵀ

Any pure state of a single qubit is a linear combination (superposition) of these basis states:

|ψ⟩ = α|0⟩ + β|1⟩

Vector representation:

|ψ⟩ = [ α , β ]ᵀ

where α and β are complex probability amplitudes such that:

|α|² + |β|² = 1



#### Quantum Gates as Matrices
Quantum logic gates manipulate qubit states. These operations are linear and can be represented using matrices. Because quantum operations must preserve total probability, these matrices must be **unitary**, meaning:

U†U = I

where U† is the conjugate transpose of U.

For example:

Pauli-X gate (Quantum NOT gate)

X = \[[0, 1],  
     [1, 0]]

Hadamard gate

H = (1/√2) × \[[1, 1],  
              [1, -1]]



#### Matrix Multiplication
When a quantum gate operates on a qubit, the operation is mathematically represented by matrix-vector multiplication.

For example, applying the X gate to |0⟩:

X|0⟩ = \[[0,1],[1,0]] × [1,0]ᵀ

Result:

[0,1]ᵀ = |1⟩

This shows that the X gate flips the state from |0⟩ to |1⟩.

When multiple quantum gates are applied sequentially, the overall operation corresponds to matrix-matrix multiplication.



#### Tensor Products (Kronecker Product)
To represent multi-qubit systems, we use the **tensor product**, denoted by ⊗.

If two qubits are in states |u⟩ and |v⟩, the combined system is:

|u⟩ ⊗ |v⟩

Example:

|0⟩ ⊗ |0⟩ = |00⟩

Vector representation:

[1,0]ᵀ ⊗ [1,0]ᵀ = [1,0,0,0]ᵀ

If gate A acts on the first qubit and gate B acts on the second qubit, the combined operation is represented as:

A ⊗ B

Tensor products allow single-qubit operations to be combined into larger multi-qubit systems.



#### Conclusion
By understanding matrix operations such as matrix multiplication and tensor products, we can predict how quantum states evolve during computation. These linear algebra operations form the mathematical foundation for quantum algorithms and quantum circuit execution.