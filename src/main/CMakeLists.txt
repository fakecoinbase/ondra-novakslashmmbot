cmake_minimum_required(VERSION 2.8) 
add_compile_options(-std=c++17)

add_executable (mmbot  
	abstractExtern.cpp
	authmapper.cpp
	ext_stockapi.cpp
	mtrader.cpp
	istockapi.cpp
	storage.cpp
	emulator.cpp
	main.cpp
	report.cpp
	webcfg.cpp	
	traders.cpp
	strategy.cpp
	strategy_halfhalf.cpp
	strategy_plfrompos.cpp
	strategy_keepvalue.cpp
	strategy_keepvalue_limited.cpp
	strategy_hypersquare.cpp
	strategy_exponencial.cpp
	strategy_sinh.cpp
	strategy_stairs.cpp
	strategy_hyperbolic.cpp
	localdailyperfmod.cpp
	extdailyperfmod.cpp
	ext_storage.cpp
	backtest.cpp
	)
target_link_libraries (mmbot LINK_PUBLIC simpleServer imtjson )
install(TARGETS mmbot DESTINATION "bin") 
