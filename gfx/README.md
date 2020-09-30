# kiss-gfx

Packaged some gfx-related builds!

:pencil2: **Image editor:**
`gimp` `grafx2`

:black_nib: **Vector graphics editor:**
`inkscape`

## kiss-hooks

In order to build `gimp` and `inkscape`, we need to set this hooks:

```shell
case $TYPE in
    pre-build)
        case $PKG in
            atk|pango)
                sed -i "s/-Dintrospection=false/-Dintrospection=true/g" "$repo_dir/build"
            ;;
            gdk-pixbuf|pango)
                sed -i "s/-Dgir=false/-Dgir=true/g"                     "$repo_dir/build"
            ;;
            gtk+3)
                sed -i "s/-introspection=no/-introspection=yes/g"       "$repo_dir/build"
            ;;
        esac
    ;;
    post-build)
        case $PKG in
            atk|pango)
                sed -i "s/-Dintrospection=true/-Dintrospection=false/g" "$repo_dir/build"
            ;;
            gdk-pixbuf|pango)
                sed -i "s/-Dgir=true/-Dgir=false/g"                     "$repo_dir/build"
            ;;
            gtk+3)
                sed -i "s/-introspection=yes/-introspection=no/g"       "$repo_dir/build"
            ;;
        esac
    ;;
esac
```

And rebuild these packages before install it:

```
~ $ kiss b atk gdk-pixbuf gtk+3 pango
~ $ kiss i atk gdk-pixbuf gtk+3 pango
```
