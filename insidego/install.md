make.bash ��ִ��
 ./cmd/dist/dist bootstrap -a -v

�������ִ��/cmd/dist/build.go���cmdboostrap() ����.
����������ȥִ��: cmd/dist/buildtools.go ��� bootstrapBuildTools()
Building Go toolchain/ 
         Generate const like version = go1.5.1, defaultGOROOT= /home/golang etc
         // Use $GOROOT/pkg/bootstrap as the bootstrap workspace root.
         // We use a subdirectory of $GOROOT/pkg because that's the
         // space within $GOROOT where we store all generated objects

copy һ���ļ��е��ļ�������һ�ݵ� $GOROOT/pkg/bootstrap/src/, �������һ��bootstrapFixImports()����.

```
 "asm",
"asm/internal/arch",
"asm/internal/asm",
"asm/internal/flags",
"asm/internal/lex",
"compile",
"compile/internal/amd64",
"compile/internal/arm",
"compile/internal/arm64",
"compile/internal/big",
"compile/internal/gc",
"compile/internal/ppc64",
"compile/internal/x86",
"internal/gcprog",
"internal/obj",
"internal/obj/arm",
"internal/obj/arm64",
"internal/obj/ppc64",
"internal/obj/x86",
"link",
"link/internal/amd64",
"link/internal/arm",
"link/internal/arm64",
"link/internal/ld",
"link/internal/ppc64",
"link/internal/x86",
```


Ȼ��ִ��```GOROOT=//home/sunan/go/src/go1.4/ GOPATH=/home/sunan/github.com/RustJason/LearningNote/go/pkg/bootstrap /home/sunan/go/src/go1.4/bin/go install -v bootstrap/...```
��ʵ����go install ������bootstrap���package.Ȼ��

