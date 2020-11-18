LevelDB qdb branch
==================

This is build successfully under vc++ 2015
with these pre-steps:
- Download the boost library 1.66 from https://sourceforge.net/projects/boost/files/boost-binaries/, I extracted to C:\Dev\libs\boost_1_66_0
- run bootstrap.bat
- run bjam.exe --toolset=msvc-14.0 --stagedir="C:\Dev\libs\boost_1_66_0\vc14" architecture=x86 address-model=32 link=static --build-type=complete --with-system --with-thread --with-date_time --with-filesystem --with-serialization
- then search all *.lib and put to this new folder
	C:\Dev\libs\boost_1_66_0\vc14
	you should have these lib files:
	
   2,119,664 libboost_chrono-vc140-mt-gd-x32-1_66.lib
     328,904 libboost_chrono-vc140-mt-s-x32-1_66.lib
   1,910,512 libboost_chrono-vc140-mt-sgd-x32-1_66.lib
     327,984 libboost_chrono-vc140-mt-x32-1_66.lib
   3,077,642 libboost_date_time-vc140-mt-gd-x32-1_66.lib
     718,446 libboost_date_time-vc140-mt-s-x32-1_66.lib
   2,932,822 libboost_date_time-vc140-mt-sgd-x32-1_66.lib
     682,382 libboost_date_time-vc140-mt-x32-1_66.lib
   6,762,912 libboost_filesystem-vc140-mt-gd-x32-1_66.lib
   1,015,928 libboost_filesystem-vc140-mt-s-x32-1_66.lib
   5,924,234 libboost_filesystem-vc140-mt-sgd-x32-1_66.lib
     958,062 libboost_filesystem-vc140-mt-x32-1_66.lib
  32,043,970 libboost_serialization-vc140-mt-gd-x32-1_66.lib
  10,634,508 libboost_serialization-vc140-mt-s-x32-1_66.lib
  32,562,536 libboost_serialization-vc140-mt-sgd-x32-1_66.lib
   9,391,454 libboost_serialization-vc140-mt-x32-1_66.lib
     748,488 libboost_system-vc140-mt-gd-x32-1_66.lib
     102,972 libboost_system-vc140-mt-s-x32-1_66.lib
     678,862 libboost_system-vc140-mt-sgd-x32-1_66.lib
     102,652 libboost_system-vc140-mt-x32-1_66.lib
   3,988,382 libboost_thread-vc140-mt-gd-x32-1_66.lib
   1,173,714 libboost_thread-vc140-mt-s-x32-1_66.lib
   3,818,862 libboost_thread-vc140-mt-sgd-x32-1_66.lib
   1,168,052 libboost_thread-vc140-mt-x32-1_66.lib
  20,643,248 libboost_wserialization-vc140-mt-gd-x32-1_66.lib
   8,638,768 libboost_wserialization-vc140-mt-s-x32-1_66.lib
  22,583,550 libboost_wserialization-vc140-mt-sgd-x32-1_66.lib
   7,236,154 libboost_wserialization-vc140-mt-x32-1_66.lib
   
- then download this github repository, open leveldb.sln with vc++ 2015
- build the solution should work

====================
This was previous readme.txt
Current version: 1.18

quasardb [LevelDB](http://code.google.com/p/leveldb/) branch with full Windows support. This is not an official LevelDB branch, but the branch we use in our product, [quasardb](https://www.quasardb.net/).

* Full Windows support: everything builds, all tests pass;
* [CMake](http://www.cmake.org/) based build
* Explicit (thread unsafe) de-allocation routines for "clean exits". Helps a lot when running your application into a leak detector;
* The Windows build requires [Boost](http://www.boost.org/); 
* Our code is C++11ish and may require a recent compiler;
* Lots of warnings fixed;
* Is not 100% compliant with Google coding style.

Tested on [FreeBSD](http://www.freebsd.org/), Linux and Windows (32-bit & 64-bit).

Might contains trace of nuts.

Comments? Questions? Suggestions? Pull!
