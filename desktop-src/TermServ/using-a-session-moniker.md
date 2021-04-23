---
title: Использование моникера сеанса
description: Активация "сеанс — сеанс" позволяет клиентскому процессу активировать локальный серверный процесс в указанном сеансе.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700d251aa1136747529b66b975d4cbedf9b14dcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338873"
---
# <a name="using-a-session-moniker"></a><span data-ttu-id="f07e7-103">Использование моникера сеанса</span><span class="sxs-lookup"><span data-stu-id="f07e7-103">Using a Session Moniker</span></span>

<span data-ttu-id="f07e7-104">Активация "сеанс — сеанс" позволяет клиентскому процессу активировать локальный серверный процесс в указанном сеансе.</span><span class="sxs-lookup"><span data-stu-id="f07e7-104">Session-to-session activation allows a client process to activate a local server process on a specified session.</span></span> <span data-ttu-id="f07e7-105">Это можно сделать отдельно для каждого сеанса, используя предоставленное системой специальное имя сеанса.</span><span class="sxs-lookup"><span data-stu-id="f07e7-105">You can do this on a per-session basis by using a system-supplied session moniker.</span></span> <span data-ttu-id="f07e7-106">Дополнительные сведения о создании моникера сеанса см. в разделе [Активация сеанса между сеансами с моникером сеанса](session-to-session-activation-with-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="f07e7-106">For more information about creating a session moniker, see [Session-to-Session Activation with a Session Moniker](session-to-session-activation-with-a-session-moniker.md).</span></span>

<span data-ttu-id="f07e7-107">В следующем примере показано, как активировать локальный серверный процесс с ИДЕНТИФИКАТОРом класса "10000013-0000-0000-0000-000000000001" в сеансе с ИДЕНТИФИКАТОРом сеанса 3.</span><span class="sxs-lookup"><span data-stu-id="f07e7-107">The following example shows how to activate a local server process with the class ID "10000013-0000-0000-0000-000000000001" on the session with the session ID 3.</span></span>

<span data-ttu-id="f07e7-108">Во-первых, пример вызывает [**функцию CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) для инициализации библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="f07e7-108">First, the sample calls the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function to initialize the COM library.</span></span> <span data-ttu-id="f07e7-109">Затем пример вызывает [**креатебиндкткс**](/windows/win32/api/objbase/nf-objbase-createbindctx) для получения указателя на реализацию интерфейса [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="f07e7-109">Then the sample calls [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) to retrieve a pointer to an implementation of the [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="f07e7-110">Этот объект хранит сведения об операциях привязки моникера. указатель необходим для вызова методов интерфейса [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="f07e7-110">This object stores information about moniker-binding operations; the pointer is required to call methods of the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="f07e7-111">Затем в примере вызывается функция [мкпарседисплайнамикс](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) для создания моникера составного сеанса, а затем метод [**IMoniker:: биндтубжект**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) для активации соединения между клиентом и сервером, используя только что созданный моникер сеанса.</span><span class="sxs-lookup"><span data-stu-id="f07e7-111">Next the sample calls the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function to create the composite session moniker and then the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to activate the connection between the client and the server process, using the newly created session moniker.</span></span> <span data-ttu-id="f07e7-112">На этом этапе можно использовать указатель интерфейса для выполнения требуемых операций с объектом.</span><span class="sxs-lookup"><span data-stu-id="f07e7-112">At this point you can use the interface pointer to perform the desired operations on the object.</span></span> <span data-ttu-id="f07e7-113">Наконец, в примере освобождается контекст привязки и вызывается функция [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="f07e7-113">Finally, the sample releases the bind context and calls the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



<span data-ttu-id="f07e7-114">Так как "{идентификатор класса моникера класса}" также является способом именования моникера класса, можно использовать следующую строку для именования составного моникера (моникер сеанса, состоящего из моникера класса), а не способом, приведенным в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="f07e7-114">Because "{class id of the class moniker}" is also a way to name a class moniker, you can use the following string to name the composite moniker (the session moniker composed with the class moniker) instead of the way show in the preceding example.</span></span>

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> <span data-ttu-id="f07e7-115">Если один и тот же пользователь вошел в каждый сеанс во время межсеансовой активации, можно успешно активировать любой серверный процесс, настроенный для запуска в режиме интерактивной активации пользователя с помощью команды RunAs.</span><span class="sxs-lookup"><span data-stu-id="f07e7-115">If the same user is logged on to each session during a cross-session activation, you can successfully activate any server process configured to run in the RunAs Interactive User activation mode.</span></span> <span data-ttu-id="f07e7-116">Если в каждый сеанс входит несколько пользователей, сервер должен вызвать функцию [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы установить соответствующие права пользователя, прежде чем произойдет успешная Активация и подключение между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="f07e7-116">If different users are logged on to each session, the server must call the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function to set the appropriate user rights before a successful activation and connection can occur between the client and the server.</span></span> <span data-ttu-id="f07e7-117">Одним из способов добиться этого является то, что сервер реализует пользовательский интерфейс [**иакцессконтрол**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) и передает реализацию в **CoInitializeSecurity**.</span><span class="sxs-lookup"><span data-stu-id="f07e7-117">One way to accomplish this would be for the server to implement a custom [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) interface and pass the implementation to **CoInitializeSecurity**.</span></span> <span data-ttu-id="f07e7-118">В любом случае пользователь клиента должен иметь соответствующие разрешения на [**Запуск**](../com/launchpermission.md) и [**доступ**](../com/accesspermission.md) , указанные в приложении, работающем на сервере.</span><span class="sxs-lookup"><span data-stu-id="f07e7-118">In any case, the client user must have the appropriate [**Launch**](../com/launchpermission.md) and [**Access Permissions**](../com/accesspermission.md) that are specified by the application running on the server.</span></span> <span data-ttu-id="f07e7-119">Дополнительные сведения см. [в разделе Безопасность в com](../com/security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f07e7-119">For more information see [Security in COM](../com/security-in-com.md).</span></span>

 

<span data-ttu-id="f07e7-120">Дополнительные сведения о предоставляемых системой моникерах, моникерах и режимах активации см. в разделе [моникеры](../com/monikers.md), интерфейс [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) и [ключ AppID](/windows/desktop/com/appid-key) в документации по com в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="f07e7-120">For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).</span></span>

 

 