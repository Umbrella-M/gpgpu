# gpgpu

This project is mainly for a gpgpu development.

1. I intend to write this project in chisel.
2. using some kind of cpu simulation for tests, should consider of circle-ci like cloud ci for verifing.
3. At the very beginning, I intend to use this repository for some technical knowledge sharing. We should put some informations and knowledges we need here.

## HW Architecture Ideas

1. The gpu should use the SIMT programming model.
2. The gpu arch should be simple(easy to understand)!! simple is the key idea.
3. May be use the unified L1 cache and register files.
4. The tensor-core can use the google TPU archtecture[1].

## SW Architecture Ideas
There will be too much effort to support cuda runtime.
We choose the easy way, basic compiler support(RISV-GPU?). And then go on use the pytorch-triton way.

thin software stack is the goal.


## timeline

1. knowledge exchange and running/test platform build, example code.
2. basic arch design for multistream processor:
    - isa design(using RISC-V?)
    - schedule arch design (buffer, decode, dispatch...)
    - vector processing units arch design(fp32 computation, int32 computation)
    - memory system desgin(L1 cache, register, sharedmemory)
3. implement & tests
4. tensor-core arch design & tests


## responsiblity and human resource

I do not want to push this project too hard, just for learning and every developer's insterests.

We should discuss in every design, and arrive on a agreement. 
Then Each part is for a maintainer to take responsiblity.

We should discuss process every week, not too much time.


[1] Kung, Hsiang-Tsung. "Why systolic architectures?." Computer 15.1 (1982): 37-46.

