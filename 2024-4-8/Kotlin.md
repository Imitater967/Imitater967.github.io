## 分模块化的思路

在使用Koin的时候,我们可以在modules引用其他模块的module,而不是都在main里创建

```

install(Koin){
    modules(
        xxxModule //good
        module{
            single<xxxManager>(xxxManagerImpl()) //good for global stuff, bad for scoped
        }        
    )
}

val xxxModule = module{
                 single<xxxManager>(xxxManagerImpl())
                }  
```

同样的,在路由的时候这么做

```
routing {
    get("/module/xxx"){} //not good enough
    registerModuleRoute() //good
}

Route.registerModuleRoute(){
    get("/module/xxx"){}
}
```

## exposed框架修改名字的地方

可以在Table("newName")酱紫