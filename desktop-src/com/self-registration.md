---
title: Self-Registration
description: Самостоятельная регистрация — это стандартный способ, с помощью которого серверный модуль может упаковывать собственные операции реестра, как регистрация, так и Отмена регистрации, в сам модуль.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488340"
---
# <a name="self-registration"></a>Self-Registration

По мере того как программное обеспечение компонентов по-новому растет как рыночное, в нем будет больше и больше экземпляров, где пользователь получает новый программный компонент в виде одной библиотеки DLL или EXE, например при скачивании нового компонента из интерактивной службы или получении одного из друга на гибком диске. В таких случаях нецелесообразно потребовать от пользователя пройти продолжительную процедуру установки или программу установки. Помимо проблем лицензирования, которые обрабатываются через [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), процедура установки обычно создает необходимые записи реестра для правильной работы компонента в контексте COM и OLE.

Самостоятельная регистрация — это стандартный способ, с помощью которого серверный модуль может упаковывать собственные операции реестра, как регистрация, так и Отмена регистрации, в сам модуль. При использовании с лицензированием, обработанном через [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), сервер может стать полностью автономным модулем без необходимости использовать внешние программы установки или reg-файлы.

Любой модуль саморегистрации (DLL или EXE) должен сначала включить строку "Олеселфрегистер" в раздел [стрингфилеинфо](/windows/desktop/menurc/stringfileinfo-block) ресурса сведений о версии, как показано ниже.

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

Существование этих данных позволяет любому заинтересованному лицу, например приложению, желающему интегрировать этот новый компонент, определить, поддерживает ли сервер самостоятельную регистрацию без необходимости предварительной загрузки DLL или EXE.

Если сервер упакован в модуль DLL, Библиотека DLL должна экспортировать функции [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Любое приложение, желающее зарегистрировать сервер (то есть все его идентификаторы CLSID и идентификаторы библиотеки типов), может получить указатель на функцию **DllRegisterServer** с помощью функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) . В рамках операции **DllRegisterServer** библиотека DLL создает все необходимые записи реестра, сохраняя правильный путь к библиотеке DLL для всех записей [InprocServer32](inprocserver32.md) или [InprocHandler32](inprochandler32.md) .

Когда приложение хочет удалить компонент из системы, необходимо отменить регистрацию этого компонента, вызвав [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). В этом вызове сервер удаляет только записи, созданные ранее в [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver). Сервер не должен самостоятельно удалять все записи для своих классов, так как другое программное обеспечение может хранить дополнительные записи, такие как [треатас](treatas.md) клавиша.

Если сервер упакован в модуль EXE, приложение, желающее зарегистрировать сервер, запускает EXE-сервер с аргументом командной строки **/regserver** или **-регсервер** (без учета регистра). Если приложению нужно отменить регистрацию сервера, он запустит EXE-файл с аргументом командной строки **/UnregServer** или **-унрегсервер**. Исполняемый файл с собственной регистрацией обнаруживает эти аргументы командной строки и вызывает те же операции, что и библиотека DLL, в [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)соответственно, регистрируя путь к модулю в разделе [LocalServer32](localserver32.md) вместо **InprocServer32** или **InprocHandler32**.

Сервер должен зарегистрировать полный путь к расположению установки модуля DLL или EXE для соответствующих разделов **InprocServer32**, **InprocHandler32** и **LocalServer32** в реестре. Путь к модулю легко получить с помощью функции [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Установка в качестве приложения службы](installing-as-a-service-application.md)
</dt> <dt>

[Регистрация класса при установке](registering-a-class-at-installation.md)
</dt> <dt>

[Регистрация работающего сервера EXE](registering-a-running-exe-server.md)
</dt> <dt>

[Регистрация объектов в таблице ROT](registering-objects-in-the-rot.md)
</dt> </dl>

 

 