File: typedefs.h



Provides convenient short-hand names for all standard data types. Naming scheme is as follows; pointers are read right-to-left to avoid naming clashes:

{state}[sign][integer/float][bits][pointers with state modifiers]

Examples:

"ui32" is 32-bit unsigned integer.

"vsi128ptrc" is constant pointer to a 128-bit volatile signed integer.

"vptrcptr" is pointer to constant pointer to volatile.

.

File: 24-bit integers.h



Provides 24-bit integers, both signed and unsigned variants. Uses same naming scheme as "typedefs.h": eg. "ui24" for 24-bit unsigned integer. All arithmetic, logic, and conversion operations with all standard data types of up to 64 bits are supported.

.

File: vector structures.h



Provides vector data types for all standard, SSE, and AVX data types, including 24-bit integers. Vector element counts range from 2 to 64. Naming scheme is similar to that of "typedefs.h":

{state}VEC[element count]D[sign][element type]

Examples:

"VEC3Ds24" is a vector of three 24-bit signed integers.

"SSE4Df32" is a vector of four 32-bit floats, for use with 128-bit SIMD operations.

"cAVX16Du16" is a constant vector of sixteen 16-bit unsigned integers, for use with 256-bit SIMD operations.

"vAVX8Df64" is a volatile vector of eight 64-bit floats, for use with 512-bit SIMD operations.

.

File: Fixed-point data types.h



Provides a broad range of fixed-point data types. There are 8, 16, 24, and 32-bit variants available, including types with a user-definable range, as well as vectors of 2 & 4 elements. Naming scheme is as follows:

{state}f{integer bits}p[fraction bits]{normalised}{[lowest value]_[highest value]}

Examples:

"fp8n" is 8 bits with a range that is user-definable.

"cfs1p14x2" is two constant 16 bits, each with a signed range of -2.0~1.99993896484375.

"fp16n_0_128" is 32 bits with a signed range of 0.0~128.0.

"fp32n_1_1" is 32 bits with a signed range of -1.0~1.0.
