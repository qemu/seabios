################ Hindawi port rules

%.h: %.h.uhin
	@echo "  Processing Hindawi ported .h header $@"
	cat $< | tail +2 | iconv -futf8 -tutf16 | uni2acii | acii2pcf | h2c > $@
	cat $@ | grep '^#include' | grep '"' | cut -d'"' -f2 |\
		 xargs -n1 -I{} make -C $(shell dirname $<) {}
	
%.c: %.c.uhin
	@echo "  Processing Hindawi ported .c source $@"
	cat $< | tail +2 | iconv -futf8 -tutf16 | uni2acii | acii2pcf | h2c > $@
	cat $@ | grep '^#include' | grep '"' | cut -d'"' -f2 |\
		 xargs -n1 -I{} make -C $(shell dirname $<) {}
		 
%.c: %.c_shipped.uhin
	@echo "  Processing _shipped source $@"
	cat $< | tail +2 | iconv -futf8 -tutf16 | uni2acii | acii2pcf | h2c > $@_shipped
	$(Q)cat $@_shipped > $@
	cat $@ | grep '^#include' | grep '"' | cut -d'"' -f2 |\
		 xargs -n1 -I{} make -C $(shell dirname $<) {}

$(obj)/%:: $(src)/%_shipped.uhin
	@echo "  Processing _shipped source $@"
	cat $< | tail +2 | iconv -futf8 -tutf16 | uni2acii | acii2pcf | h2c > $@_shipped
	$(Q)cat $@_shipped > $@
	cat $@ | grep '^#include' | grep '"' | cut -d'"' -f2 |\
		 xargs -n1 -I{} make -C $(shell dirname $<) {}

#####################################
