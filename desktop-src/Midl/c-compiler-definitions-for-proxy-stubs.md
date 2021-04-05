---
title: Определения для прокси-сервера и заглушек C-компилятора
description: Файл заголовка RPCProxy. h содержит следующие определения макросов, каждый из которых удобен при создании распределенного приложения COM. Эти макросы вызываются с параметром препроцессора/D (или-D) во время компиляции C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL компилятора MIDL, C-Compiler, определения прокси-сервера или заглушек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068370"
---
# <a name="c-compiler-definitions-for-proxystubs"></a><span data-ttu-id="d69b5-105">Определения для прокси-сервера и заглушек C-компилятора</span><span class="sxs-lookup"><span data-stu-id="d69b5-105">C-Compiler Definitions for Proxy/Stubs</span></span>

<span data-ttu-id="d69b5-106">Файл заголовка RPCProxy. h содержит следующие определения макросов, каждый из которых удобен при создании распределенного приложения COM.</span><span class="sxs-lookup"><span data-stu-id="d69b5-106">The header file Rpcproxy.h includes the following macro definitions, each of which may be convenient when building distributed COM application.</span></span> <span data-ttu-id="d69b5-107">Эти макросы вызываются с параметром препроцессора [**/d**](-d.md) (или-D) во время компиляции C.</span><span class="sxs-lookup"><span data-stu-id="d69b5-107">These macros are invoked with the [**/D**](-d.md) (or -D) preprocessor switch at the C-compile time.</span></span>



| <span data-ttu-id="d69b5-108">MACRO</span><span class="sxs-lookup"><span data-stu-id="d69b5-108">MACRO</span></span>                                                                                                                                                                                           | <span data-ttu-id="d69b5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d69b5-109">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69b5-110">ЗАРЕГИСТРИРОВАТЬ \_ прокси- \_ библиотеку DLL</span><span class="sxs-lookup"><span data-stu-id="d69b5-110">REGISTER\_PROXY\_DLL</span></span>                                                                                                                                                                            | <span data-ttu-id="d69b5-111">Создает функции **DllMain**, **DllRegisterServer** и **DllUnregisterServer** для автоматической регистрации библиотеки DLL прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="d69b5-111">Generates **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions for automatically registering a proxy DLL.</span></span>                                                                                       |
| <span data-ttu-id="d69b5-112">прокси-сервер \_ CLSID =<clsid></span><span class="sxs-lookup"><span data-stu-id="d69b5-112">PROXY\_CLSID=<clsid></span></span>                                                                                                                                                                      | <span data-ttu-id="d69b5-113">Указывает идентификатор класса для сервера.</span><span class="sxs-lookup"><span data-stu-id="d69b5-113">Specifies a class identifier for the server.</span></span> <span data-ttu-id="d69b5-114">Если этот макрос не определен, то CLSID по умолчанию — это первый идентификатор интерфейса, который компилятор MIDL обнаруживает в спецификации IDL для прокси-сервера/заглушки.</span><span class="sxs-lookup"><span data-stu-id="d69b5-114">If this macro is not defined, the default CLSID is the first interface identifier that the MIDL compiler encounters in the IDL specification for the Proxy/Stub server.</span></span> |
| <span data-ttu-id="d69b5-115">Прокси-сервер \_ CLSID \_ — это = {0x *8hexdigits*, 0x *4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits,*}}</span><span class="sxs-lookup"><span data-stu-id="d69b5-115">PROXY\_CLSID\_IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}}</span></span> | <span data-ttu-id="d69b5-116">Указывает значение идентификатора класса сервера в двоичном шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="d69b5-116">Specifies the value of the server's class identifier in binary hex format.</span></span>                                                                                                                                           |



 

<span data-ttu-id="d69b5-117">Определив макрос **Register \_ Proxy \_ DLL** при компиляции DLLDATA. c, Библиотека DLL для маршалирования прокси-сервера и заглушки автоматически включит определения по умолчанию для функций **DllMain**, **DllRegisterServer** и **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="d69b5-117">By defining the **REGISTER\_PROXY\_DLL** macro when compiling Dlldata.c, your proxy/stub marshaling DLL will automatically include default definitions for the **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions.</span></span> <span data-ttu-id="d69b5-118">Эти функции можно использовать для самостоятельной регистрации библиотеки DLL прокси-сервера в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="d69b5-118">You can use these functions to self-register your proxy DLL in the system registry.</span></span>

<span data-ttu-id="d69b5-119">Этот код регистрации по умолчанию использует идентификатор GUID первого интерфейса, обнаруженного в качестве идентификатора CLSID для регистрации всего сервера DLL прокси или заглушки.</span><span class="sxs-lookup"><span data-stu-id="d69b5-119">This default registration code uses the GUID of the first interface encountered as the CLSID for registering the entire proxy/stub DLL server.</span></span> <span data-ttu-id="d69b5-120">COM позже использует этот идентификатор CLSID для нахождение и загрузки скомпилированного прокси-сервера/заглушки для упаковки любого из интерфейсов, регистрируемых сервером для работы.</span><span class="sxs-lookup"><span data-stu-id="d69b5-120">COM later uses this CLSID to locate and load the compiled proxy/stub server for the marshaling of any of the interfaces the server is registered to handle.</span></span> <span data-ttu-id="d69b5-121">Когда приложение выполняет вызов метода интерфейса, который пересекает границы потока, процесса или компьютера, COM использует запись реестра идентификатор интерфейса для нахождение записи реестра CLSID для сервера маршалинга прокси или заглушки.</span><span class="sxs-lookup"><span data-stu-id="d69b5-121">When an application makes an interface method call that crosses thread, process, or computer boundaries, COM uses the interface identifier registry entry to locate the CLSID registry entry for the proxy/stub marshaling server.</span></span> <span data-ttu-id="d69b5-122">Затем он использует этот идентификатор CLSID для загрузки сервера (если он еще не загружен), чтобы вызов интерфейса мог быть маршалирован.</span><span class="sxs-lookup"><span data-stu-id="d69b5-122">It then uses this CLSID to load the server (if it isn't already loaded) so that the interface call can then be marshaled.</span></span>

<span data-ttu-id="d69b5-123">Используйте макрос **прокси-сервера \_ CLSID** , = <clsid> Если нужно явно указать идентификатор CLSID прокси-сервера или заглушки, а не использовать CLSID по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d69b5-123">Use the **PROXY\_CLSID**=<clsid> macro when you want to explicitly specify the proxy/stub server's CLSID rather than rely on the default CLSID.</span></span> <span data-ttu-id="d69b5-124">Например, если вы создаете стандартную библиотеку DLL для маршалирования в качестве собственного внутрипроцессного COM-сервера или необходимо определить собственную функцию **DllMain** для обработки \_ присоединения к процессу DLL \_ .</span><span class="sxs-lookup"><span data-stu-id="d69b5-124">For example, if you are building a standard marshaling DLL as your own in-process COM server, or if you need to define your own **DllMain** to handle DLL\_PROCESS\_ATTACH.</span></span>

<span data-ttu-id="d69b5-125">Используйте **прокси-сервер \_ CLSID \_ — это** макрос вместо **\_ CLSID прокси-сервера** , чтобы определить значение идентификатора CLSID в двоичном шестнадцатеричном формате, используемом в макросе **define \_ GUID** .</span><span class="sxs-lookup"><span data-stu-id="d69b5-125">Use **PROXY\_CLSID\_IS**= macro instead of **PROXY\_CLSID** to define the value of the CLSID in the binary hexadecimal format that the **DEFINE\_GUID** macro uses.</span></span>

<span data-ttu-id="d69b5-126">Также обратите внимание, что при выполнении функции **DllRegisterServer** по умолчанию она регистрирует сервер с помощью ThreadingModel = Both.</span><span class="sxs-lookup"><span data-stu-id="d69b5-126">Also note that when the default **DllRegisterServer** function runs, it registers the server with ThreadingModel=Both.</span></span>

<span data-ttu-id="d69b5-127">В следующем примере файла makefile используется **\_ прокси- \_ Библиотека Register** и **прокси-сервер \_ CLSID**=.</span><span class="sxs-lookup"><span data-stu-id="d69b5-127">The following makefile example uses the **REGISTER\_PROXY\_DLL** and **PROXY\_CLSID**= macros:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

<span data-ttu-id="d69b5-128">Дополнительные сведения о параметре препроцессора [**/d**](-d.md) см. в документации по компилятору C.</span><span class="sxs-lookup"><span data-stu-id="d69b5-128">For more information on the [**/D**](-d.md) preprocessor option, see your C compiler documentation.</span></span>

 

 




