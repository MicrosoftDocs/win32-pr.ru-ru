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
# <a name="self-registration"></a><span data-ttu-id="0251a-103">Self-Registration</span><span class="sxs-lookup"><span data-stu-id="0251a-103">Self-Registration</span></span>

<span data-ttu-id="0251a-104">По мере того как программное обеспечение компонентов по-новому растет как рыночное, в нем будет больше и больше экземпляров, где пользователь получает новый программный компонент в виде одной библиотеки DLL или EXE, например при скачивании нового компонента из интерактивной службы или получении одного из друга на гибком диске.</span><span class="sxs-lookup"><span data-stu-id="0251a-104">As component software continues to grow as a market, there will be more and more instances where a user obtains a new software component as a single DLL or EXE module, such as when downloading a new component from an on-line service or receiving one from a friend on a floppy disk.</span></span> <span data-ttu-id="0251a-105">В таких случаях нецелесообразно потребовать от пользователя пройти продолжительную процедуру установки или программу установки.</span><span class="sxs-lookup"><span data-stu-id="0251a-105">In these cases, it is not practical to require the user to go through a lengthy installation procedure or setup program.</span></span> <span data-ttu-id="0251a-106">Помимо проблем лицензирования, которые обрабатываются через [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), процедура установки обычно создает необходимые записи реестра для правильной работы компонента в контексте COM и OLE.</span><span class="sxs-lookup"><span data-stu-id="0251a-106">Besides the licensing issues, which are handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), an installation procedure typically creates the necessary registry entries for a component to run properly in the COM and OLE context.</span></span>

<span data-ttu-id="0251a-107">Самостоятельная регистрация — это стандартный способ, с помощью которого серверный модуль может упаковывать собственные операции реестра, как регистрация, так и Отмена регистрации, в сам модуль.</span><span class="sxs-lookup"><span data-stu-id="0251a-107">Self-registration is the standard means through which a server module can package its own registry operations, both registration and unregistration, into the module itself.</span></span> <span data-ttu-id="0251a-108">При использовании с лицензированием, обработанном через [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), сервер может стать полностью автономным модулем без необходимости использовать внешние программы установки или reg-файлы.</span><span class="sxs-lookup"><span data-stu-id="0251a-108">When used with licensing handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), a server can become an entirely self-contained module with no need for external installation programs or .reg files.</span></span>

<span data-ttu-id="0251a-109">Любой модуль саморегистрации (DLL или EXE) должен сначала включить строку "Олеселфрегистер" в раздел [стрингфилеинфо](/windows/desktop/menurc/stringfileinfo-block) ресурса сведений о версии, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="0251a-109">Any self-registering module, DLL or EXE, should first include an "OleSelfRegister" string in the [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) section of its version information resource, as shown here.</span></span>

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

<span data-ttu-id="0251a-110">Существование этих данных позволяет любому заинтересованному лицу, например приложению, желающему интегрировать этот новый компонент, определить, поддерживает ли сервер самостоятельную регистрацию без необходимости предварительной загрузки DLL или EXE.</span><span class="sxs-lookup"><span data-stu-id="0251a-110">The existence of this data allows any interested party, such as an application that wishes to integrate this new component, to determine whether the server supports self-registration without having to load the DLL or EXE first.</span></span>

<span data-ttu-id="0251a-111">Если сервер упакован в модуль DLL, Библиотека DLL должна экспортировать функции [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="0251a-111">If the server is packaged in a DLL module, the DLL must export the functions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="0251a-112">Любое приложение, желающее зарегистрировать сервер (то есть все его идентификаторы CLSID и идентификаторы библиотеки типов), может получить указатель на функцию **DllRegisterServer** с помощью функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0251a-112">Any application that wishes to instruct the server to register itself (that is, all its CLSIDs and type library IDs) can obtain a pointer to **DllRegisterServer** through the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function.</span></span> <span data-ttu-id="0251a-113">В рамках операции **DllRegisterServer** библиотека DLL создает все необходимые записи реестра, сохраняя правильный путь к библиотеке DLL для всех записей [InprocServer32](inprocserver32.md) или [InprocHandler32](inprochandler32.md) .</span><span class="sxs-lookup"><span data-stu-id="0251a-113">Within **DllRegisterServer**, the DLL creates all its necessary registry entries, storing the correct path to the DLL for all [InprocServer32](inprocserver32.md) or [InprocHandler32](inprochandler32.md) entries.</span></span>

<span data-ttu-id="0251a-114">Когда приложение хочет удалить компонент из системы, необходимо отменить регистрацию этого компонента, вызвав [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="0251a-114">When an application wishes to remove the component from the system, it should unregister that component by calling [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="0251a-115">В этом вызове сервер удаляет только записи, созданные ранее в [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="0251a-115">Within this call, the server removes exactly those entries it previously created in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span> <span data-ttu-id="0251a-116">Сервер не должен самостоятельно удалять все записи для своих классов, так как другое программное обеспечение может хранить дополнительные записи, такие как [треатас](treatas.md) клавиша.</span><span class="sxs-lookup"><span data-stu-id="0251a-116">The server should not blindly remove all entries for its classes because other software may have stored additional entries, such as a [TreatAs](treatas.md) key.</span></span>

<span data-ttu-id="0251a-117">Если сервер упакован в модуль EXE, приложение, желающее зарегистрировать сервер, запускает EXE-сервер с аргументом командной строки **/regserver** или **-регсервер** (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="0251a-117">If the server is packaged in an EXE module, the application wishing to register the server launches the EXE server with the command-line argument **/RegServer** or **-RegServer** (case-insensitive).</span></span> <span data-ttu-id="0251a-118">Если приложению нужно отменить регистрацию сервера, он запустит EXE-файл с аргументом командной строки **/UnregServer** или **-унрегсервер**.</span><span class="sxs-lookup"><span data-stu-id="0251a-118">If the application wishes to unregister the server, it launches the EXE with the command-line argument **/UnregServer** or **-UnregServer**.</span></span> <span data-ttu-id="0251a-119">Исполняемый файл с собственной регистрацией обнаруживает эти аргументы командной строки и вызывает те же операции, что и библиотека DLL, в [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)соответственно, регистрируя путь к модулю в разделе [LocalServer32](localserver32.md) вместо **InprocServer32** или **InprocHandler32**.</span><span class="sxs-lookup"><span data-stu-id="0251a-119">The self-registering EXE detects these command-line arguments and invokes the same operations as a DLL would within [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectively, registering its module path under [LocalServer32](localserver32.md) instead of **InprocServer32** or **InprocHandler32**.</span></span>

<span data-ttu-id="0251a-120">Сервер должен зарегистрировать полный путь к расположению установки модуля DLL или EXE для соответствующих разделов **InprocServer32**, **InprocHandler32** и **LocalServer32** в реестре.</span><span class="sxs-lookup"><span data-stu-id="0251a-120">The server must register the full path to the installation location of the DLL or EXE module for their respective **InprocServer32**, **InprocHandler32**, and **LocalServer32** keys in the registry.</span></span> <span data-ttu-id="0251a-121">Путь к модулю легко получить с помощью функции [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="0251a-121">The module path is easily obtained through the [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0251a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="0251a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0251a-123">Установка в качестве приложения службы</span><span class="sxs-lookup"><span data-stu-id="0251a-123">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="0251a-124">Регистрация класса при установке</span><span class="sxs-lookup"><span data-stu-id="0251a-124">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="0251a-125">Регистрация работающего сервера EXE</span><span class="sxs-lookup"><span data-stu-id="0251a-125">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="0251a-126">Регистрация объектов в таблице ROT</span><span class="sxs-lookup"><span data-stu-id="0251a-126">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> </dl>

 

 