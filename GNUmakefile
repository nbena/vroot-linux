NAME = imunes/template
subdirs = $(filter-out common/, $(filter %/, $(wildcard */)))
TAGS = latest $(subdirs:%/=%)
clean_TAGS = $(addprefix clean_,$(TAGS))
push_TAGS = $(addprefix push_,$(TAGS))

.PHONY: $(TAGS) $(clean_TAGS) $(push_TAGS)

info:
	@echo	"To print all imunes images: make print"
	@echo	"To build an image use: make name"
	@echo	"To remove an image use: make clean_name"
	@echo	"To push an image use: make push_name"
	@echo	"To build all images use: make build_all"
	@echo	"To remove all images use: make clean_all"
	@echo	"To push all images use: make push_all"

print:
	docker images $(NAME)

$(TAGS):
	./build.sh $@

$(clean_TAGS):
	docker rmi $(NAME):$(patsubst clean_%,%,$@)

$(push_TAGS):
	docker push $(NAME):$(patsubst push_%,%,$@)

build_all: $(TAGS)

clean_all:
	for tag in $(TAGS); do \
		docker rmi $(NAME):$$tag ; \
	done 

push_all:
	for tag in $(TAGS); do \
		docker push $(NAME):$$tag ; \
	done 