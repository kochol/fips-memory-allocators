# CMake entry point
    fips_begin_lib(memory-allocators)

        fips_dir(src)
        fips_files(
            Allocator.cpp 
            CAllocator.cpp 
            LinearAllocator.cpp 
            StackAllocator.cpp
            PoolAllocator.cpp
            FreeListAllocator.cpp 
        )

    fips_end_lib(memory-allocators)
