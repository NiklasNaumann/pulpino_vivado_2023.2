PROJECT:=xilinx_clock_manager

all:
	vivado -mode batch -source tcl/run.tcl
	mkdir -p ip
	cp ${PROJECT}.gen/sources_1/ip/${PROJECT}/${PROJECT}.dcp ip/
	cp ${PROJECT}.gen/sources_1/ip/${PROJECT}/${PROJECT}_stub.v ip/

gui:
	vivado -mode gui -source tcl/run.tcl &

clean:
	rm -rf ip/*
	mkdir -p ip
	rm -rf ${PROJECT}.xpr
	rm -rf ${PROJECT}.hw
	rm -rf ${PROJECT}.data
	rm -rf ${PROJECT}.runs
	rm -rf ${PROJECT}.srcs
	rm -rf ${PROJECT}.cache
	rm -rf ${PROJECT}.gen
	rm -rf ${PROJECT}.ip_user_files
	rm -rf component.xml
	rm -rf vivado*.jou
	rm -rf vivado*.log
	rm -rf vivado*.str
	rm -rf xgui
	rm -rf .Xil

