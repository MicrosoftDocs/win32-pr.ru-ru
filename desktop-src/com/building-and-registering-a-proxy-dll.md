---
title: Создание и регистрация библиотеки DLL прокси-сервера
description: Если для приложения выбрано маршалирование прокси-сервера или заглушки, то файлы c и h, созданные MIDL, должны быть скомпилированы и связаны для создания прокси-библиотеки DLL, и эта библиотека DLL должна быть введена в системный реестр, чтобы клиенты могли искать интерфейсы.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634cb7a17551a4b7925d0be3065c71037cc1d7ae8bf28c10fcdaee74771c302e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048852"
---
# <a name="building-and-registering-a-proxy-dll"></a>Создание и регистрация библиотеки DLL прокси-сервера

Если для приложения выбрано маршалирование прокси-сервера или заглушки, то файлы c и h, созданные MIDL, должны быть скомпилированы и связаны для создания прокси-библиотеки DLL, и эта библиотека DLL должна быть введена в системный реестр, чтобы клиенты могли искать интерфейсы. Созданный с помощью MIDL файл DLLDATA. c содержит необходимые подпрограммы и другие сведения для создания и регистрации библиотеки DLL прокси-сервера или заглушки.

Первый шаг в создании библиотеки DLL заключается в написании файла определения модуля для компоновщика, как показано в следующем примере:

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

Кроме того, эти экспортированные функции можно указать в командной строке КОМПОНОВКИ файла makefile.

Экспортированные функции объявляются в RPCProxy. h, который включает DLLDATA. c, а реализации по умолчанию являются частью библиотеки времени выполнения RPC. COM использует эти функции для создания фабрики классов, выгрузки библиотек DLL (после того, как убедитесь, что объекты или блокировки отсутствуют), извлеките сведения о прокси-библиотеке и самостоятельно Зарегистрируйте и отмените регистрацию DLL-библиотеки прокси. Чтобы воспользоваться этими предопределенными функциями, необходимо вызвать параметр Кпрепроцессор/D (или-D) при компиляции файлов DLLDATA. c и example \_ . c, как показано в следующем файле Makefile:

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

Если эти определения препроцессора не заданы во время компиляции, эти функции не определяются автоматически. (То есть макросы в папке RPCProxy. c расширяются на Nothing.) Их придется явно определить в другом исходном файле, модуль которого также будет включен в окончательную компоновку и компиляцию в командной строке компилятора C.

Когда \_ определена библиотека регистрации прокси-сервера \_ , RPCProxy. h предоставляет дополнительные элементы управления условной компиляцией с прокси-сервером \_ CLSID =*GUID*, прокси-сервер \_ CLSID \_ — это *явное значение идентификатора GUID* и Строка префикса входа \_ =*префикс строки*. Эти определения макросов более подробно описаны в [определении языка C-компилятора для прокси-серверов и заглушек](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) в документации программиста MIDL.

## <a name="manually-registering-the-proxy-dll"></a>Регистрация библиотеки DLL прокси-сервера вручную

Если по каким-либо причинам вы не можете использовать подпрограммы регистрации заглушек прокси по умолчанию, можно зарегистрировать библиотеку DLL вручную, добавив следующие записи в системный реестр с помощью Regedt32.exe.

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Определения для прокси-сервера и заглушек C-компилятора](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> <dt>

[Самостоятельная регистрация](self-registration.md)
</dt> </dl>

 

 
