---
title: Создание и регистрация библиотеки DLL прокси-сервера
description: Если для приложения выбрано маршалирование прокси-сервера или заглушки, то файлы c и h, созданные MIDL, должны быть скомпилированы и связаны для создания прокси-библиотеки DLL, и эта библиотека DLL должна быть введена в системный реестр, чтобы клиенты могли искать интерфейсы.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d4cafbe2be56d9e9a02a451e3daf905496c424
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826809"
---
# <a name="building-and-registering-a-proxy-dll"></a><span data-ttu-id="43a8f-103">Создание и регистрация библиотеки DLL прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="43a8f-103">Building and Registering a Proxy DLL</span></span>

<span data-ttu-id="43a8f-104">Если для приложения выбрано маршалирование прокси-сервера или заглушки, то файлы c и h, созданные MIDL, должны быть скомпилированы и связаны для создания прокси-библиотеки DLL, и эта библиотека DLL должна быть введена в системный реестр, чтобы клиенты могли искать интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="43a8f-104">If you chose proxy/stub marshaling for your application, the .c and .h files that MIDL generated must be compiled and linked to create a proxy DLL, and that DLL must be entered into the system registry so that clients can locate your interfaces.</span></span> <span data-ttu-id="43a8f-105">Созданный с помощью MIDL файл DLLDATA. c содержит необходимые подпрограммы и другие сведения для создания и регистрации библиотеки DLL прокси-сервера или заглушки.</span><span class="sxs-lookup"><span data-stu-id="43a8f-105">The MIDL-generated file Dlldata.c contains the necessary routines and other information to build and register a proxy/stub DLL.</span></span>

<span data-ttu-id="43a8f-106">Первый шаг в создании библиотеки DLL заключается в написании файла определения модуля для компоновщика, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="43a8f-106">The first step in building the DLL is to write a module definition file for the linker, as shown in the following example:</span></span>

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

<span data-ttu-id="43a8f-107">Кроме того, эти экспортированные функции можно указать в командной строке КОМПОНОВКИ файла makefile.</span><span class="sxs-lookup"><span data-stu-id="43a8f-107">Alternatively, you can specify these exported functions on the LINK command line of your makefile.</span></span>

<span data-ttu-id="43a8f-108">Экспортированные функции объявляются в RPCProxy. h, который включает DLLDATA. c, а реализации по умолчанию являются частью библиотеки времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="43a8f-108">The exported functions are declared in Rpcproxy.h, which Dlldata.c includes, and default implementations are part of the RPC run-time library.</span></span> <span data-ttu-id="43a8f-109">COM использует эти функции для создания фабрики классов, выгрузки библиотек DLL (после того, как убедитесь, что объекты или блокировки отсутствуют), извлеките сведения о прокси-библиотеке и самостоятельно Зарегистрируйте и отмените регистрацию DLL-библиотеки прокси.</span><span class="sxs-lookup"><span data-stu-id="43a8f-109">COM uses these functions to create a class factory, unload DLLs (after making sure that no objects or locks exist), retrieve information about the proxy DLL, and to self-register and unregister the proxy DLL.</span></span> <span data-ttu-id="43a8f-110">Чтобы воспользоваться этими предопределенными функциями, необходимо вызвать параметр Кпрепроцессор/D (или-D) при компиляции файлов DLLDATA. c и example \_ . c, как показано в следующем файле Makefile:</span><span class="sxs-lookup"><span data-stu-id="43a8f-110">To take advantage of these predefined functions, you need to invoke the Cpreprocessor /D (or -D) option when you compile the Dlldata.c and Example\_p.c files, as shown in the following makefile:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

<span data-ttu-id="43a8f-111">Если эти определения препроцессора не заданы во время компиляции, эти функции не определяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="43a8f-111">If you do not specify these preprocessor definitions at compile time, these functions are not automatically defined.</span></span> <span data-ttu-id="43a8f-112">(То есть макросы в папке RPCProxy. c расширяются на Nothing.) Их придется явно определить в другом исходном файле, модуль которого также будет включен в окончательную компоновку и компиляцию в командной строке компилятора C.</span><span class="sxs-lookup"><span data-stu-id="43a8f-112">(That is, the macros in Rpcproxy.c expand to nothing.) You would have to have defined them explicitly in another source file, whose module would also be included in the final linking and compilation on the C compiler command line.</span></span>

<span data-ttu-id="43a8f-113">Когда \_ определена библиотека регистрации прокси-сервера \_ , RPCProxy. h предоставляет дополнительные элементы управления условной компиляцией с прокси-сервером \_ CLSID =*GUID*, прокси-сервер \_ CLSID \_ — это *явное значение идентификатора GUID* и Строка префикса входа \_ =*префикс строки*.</span><span class="sxs-lookup"><span data-stu-id="43a8f-113">When REGISTER\_PROXY\_DLL is defined, Rpcproxy.h provides for additional conditional compilation control with PROXY\_CLSID=*guid*, PROXY\_CLSID\_IS=*explicit value of guid*, and ENTRY\_PREFIX=*prefix string*.</span></span> <span data-ttu-id="43a8f-114">Эти определения макросов более подробно описаны в [определении языка C-компилятора для прокси-серверов и заглушек](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) в документации программиста MIDL.</span><span class="sxs-lookup"><span data-stu-id="43a8f-114">These macro definitions are described in greater detail in [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in the MIDL Programmer's Guide.</span></span>

## <a name="manually-registering-the-proxy-dll"></a><span data-ttu-id="43a8f-115">Регистрация библиотеки DLL прокси-сервера вручную</span><span class="sxs-lookup"><span data-stu-id="43a8f-115">Manually Registering the Proxy DLL</span></span>

<span data-ttu-id="43a8f-116">Если по каким-либо причинам вы не можете использовать подпрограммы регистрации заглушек прокси по умолчанию, можно зарегистрировать библиотеку DLL вручную, добавив следующие записи в системный реестр с помощью Regedt32.exe.</span><span class="sxs-lookup"><span data-stu-id="43a8f-116">If for some reason you cannot use the default proxy stub registration routines, you can manually register the DLL by adding the following entries to the system registry, using Regedt32.exe.</span></span>

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a><span data-ttu-id="43a8f-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="43a8f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43a8f-118">Определения для прокси-сервера и заглушек C-компилятора</span><span class="sxs-lookup"><span data-stu-id="43a8f-118">C-Compiler Definitions for Proxy/Stubs</span></span>](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[<span data-ttu-id="43a8f-119">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="43a8f-119">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="43a8f-120">Самостоятельная регистрация</span><span class="sxs-lookup"><span data-stu-id="43a8f-120">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 
