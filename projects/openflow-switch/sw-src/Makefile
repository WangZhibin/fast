all: lib.a  
	gcc -o FAST ../../../lib/software/channel/openflow-2lfs/main.c lib.a -lm -lnet -lpcap -lpthread 

lib.a:
	gcc -c ../../../lib/software/services/bv-2lfs/compare.c -lm -o compare.o
	gcc -c ../../../lib/software/services/bv-2lfs/get_new_a.c -lm -o get_new_a.o
	gcc -c ../../../lib/software/services/bv-2lfs/two_to_ten.c -lm -o two_to_ten.o
	gcc -c ../../../lib/software/services/bv-2lfs/ten_to_two.c -lm -o ten_to_two.o
	gcc -c ../../../lib/software/services/bv-2lfs/six_to_two.c -lm -o six_to_two.o
	gcc -c ../../../lib/software/services/bv-2lfs/ten_to_char.c -lm -o ten_to_char.o
	gcc -c ../../../lib/software/services/bv-2lfs/eight_to_two.c -lm -o eight_to_two.o
	gcc -c ../../../lib/software/services/bv-2lfs/struct_to_char.c -lm -o struct_to_char.o
	gcc -c ../../../lib/software/services/bv-2lfs/get_mask.c -lm -o get_mask.o
	gcc -c ../../../lib/software/services/bv-2lfs/build_addr.c -lm -o build_addr.o
	gcc -c ../../../lib/software/services/bv-2lfs/check.c -lm -o check.o
	gcc -c ../../../lib/software/platform/NetMagicPro/npe_handle.c -lpcap -lnet -o npe_handle.o
	gcc -c ../../../lib/software/services/bv-2lfs/addr_to_rule.c -I ../../../lib/software/platform/NetMagicPro/ -lm -o addr_to_rule.o
	gcc -c ../../../lib/software/services/bv-2lfs/add_rule.c -I ../../../lib/software/platform/NetMagicPro/ -lm -o add_rule.o
	gcc -c ../../../lib/software/services/bv-2lfs/get_addr.c -lm -o get_addr.o
	gcc -c ../../../lib/software/services/bv-2lfs/find_place.c -lm -o find_place.o
	gcc -c ../../../lib/software/services/bv-2lfs/find_num_of_place.c -lm -o find_num_of_place.o
	gcc -c ../../../lib/software/services/bv-2lfs/write_actions.c -I ../../../lib/software/platform/NetMagicPro/ -lm -o write_actions.o
	gcc -c ../../../lib/software/services/bv-2lfs/delete_rule.c -I ../../../lib/software/platform/NetMagicPro/ -lm -o delete_rule.o
	gcc -c ../../../lib/software/services/bv-2lfs/get_vector.c -lm -o get_vector.o
	gcc -c ../../../lib/software/services/bv-2lfs/get_bv.c -o get_bv.o
	gcc -c ../../../lib/software/services/bv-2lfs/read_addr.c -lm -o read_addr.o
	gcc -c ../../../lib/software/services/bv-2lfs/write_table.c -o write_table.o
	gcc -c ../../../lib/software/channel/openflow-2lfs/md5.c -o md5.o
	gcc -c ../../../lib/software/channel/openflow-2lfs/ofp_demo.c -I ../../../lib/software/services/bv-2lfs/ -lpcap -lnet -lpthread -o ofp_demo.o
	ar -rcs lib.a addr_to_rule.o md5.o ofp_demo.o get_new_a.o ten_to_two.o compare.o two_to_ten.o six_to_two.o eight_to_two.o ten_to_char.o struct_to_char.o get_mask.o npe_handle.o build_addr.o add_rule.o get_addr.o find_place.o find_num_of_place.o delete_rule.o check.o get_vector.o get_bv.o read_addr.o write_table.o write_actions.o
clean:
	rm -rf *.o lib.a FAST
