	CC = gcc
	OBJ = test.o max.o min.o var.o
	ifeq ($(DEBUG),yes)
		CC_OPTIONS= -g -Wall
	else
		CC_OPTIONS=
	endif

Install:	My-binaire
	mv My-binaire /home/safia
		
My-binaire:	 ${OBJ}
	${CROSS_COMPILE}${CC} ${CC_OPTIONS} ${OBJ} -o $@
ifeq	($(DEBUG),yes)

	@echo "Génération en mode Debug"

else
	
	@echo "Génération en mode Release"

endif	

max.o:	max.c
	${CROSS_COMPILE}${CC} ${CC_OPTIONS} -c $< -o $@ 
min.o:	min.c
	${CROSS_COMPILE}${CC} ${CC_OPTIONS} -c $< -o $@
var.o:	var.c
	${CROSS_COMPILE}${CC} ${CC_OPTIONS} -c $< -o $@

test.o:	test.c
	${CROSS_COMPILE}${CC} ${CC_OPTIONS} -c $^ -o $@
clean: 
	rm ${OBJ}


