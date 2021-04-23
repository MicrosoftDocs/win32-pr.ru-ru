---
title: Регистрация сервера DLL для активации суррогатных символов
description: Регистрация сервера DLL для активации суррогатных символов
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793999"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a><span data-ttu-id="f7ed6-103">Регистрация сервера DLL для активации суррогатных символов</span><span class="sxs-lookup"><span data-stu-id="f7ed6-103">Registering the DLL Server for Surrogate Activation</span></span>

<span data-ttu-id="f7ed6-104">Сервер DLL будет загружен в суррогатный процесс при следующих условиях:</span><span class="sxs-lookup"><span data-stu-id="f7ed6-104">A DLL server will be loaded into a surrogate process under the following conditions:</span></span>

-   <span data-ttu-id="f7ed6-105">В ключе CLSID в реестре должно быть указано значение AppID и соответствующий ключ [AppID](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ed6-105">There must be an AppID value specified under the CLSID key in the registry, and a corresponding [AppID](appid-key.md) key.</span></span>
-   <span data-ttu-id="f7ed6-106">При вызове активации устанавливается бит [**\_ локального \_ сервера клскткс**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , а в ключе CLSID не указывается [LocalServer32](localserver32.md), [локалсервер](localserver.md)или [LocalService](localservice.md).</span><span class="sxs-lookup"><span data-stu-id="f7ed6-106">In an activation call, the [**CLSCTX\_LOCAL\_SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) bit is set and the CLSID key does not specify [LocalServer32](localserver32.md), [LocalServer](localserver.md), or [LocalService](localservice.md).</span></span> <span data-ttu-id="f7ed6-107">Если заданы другие биты **клскткс** , то следует соблюдать [**алгоритм обработки**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)для флагов внутрипроцессного, локального или удаленного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-107">If other **CLSCTX** bits are set, the [**processing algorithm**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)for the in-process, local, or remote execution flags is followed.</span></span>
-   <span data-ttu-id="f7ed6-108">Ключ CLSID содержит подраздел [InprocServer32](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ed6-108">The CLSID key contains the [InprocServer32](inprocserver32.md) subkey.</span></span>
-   <span data-ttu-id="f7ed6-109">Прокси-Библиотека DLL или заглушка, указанная в ключе **InprocServer32** , существует.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-109">The proxy/stub DLL specified in the **InprocServer32** key exists.</span></span>
-   <span data-ttu-id="f7ed6-110">Значение [дллсуррогате](dllsurrogate.md) существует в ключе **AppID** .</span><span class="sxs-lookup"><span data-stu-id="f7ed6-110">The [DllSurrogate](dllsurrogate.md) value exists under the **AppID** key.</span></span>

<span data-ttu-id="f7ed6-111">Если имеется **локалсервер**, **LocalServer32** или **LocalService**, указывающий на существование exe-файла, то сервер или служба exe всегда будут запускаться в предпочтение для загрузки сервера DLL в суррогатный процесс.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-111">If there is a **LocalServer**, **LocalServer32**, or **LocalService**, indicating the existence of an EXE, the EXE server or service will always be launched in preference to loading a DLL server into a surrogate process.</span></span>

<span data-ttu-id="f7ed6-112">Для выполнения суррогатной активации необходимо указать **дллсуррогате** именованное значение.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-112">The **DllSurrogate** named-value must be specified for surrogate activation to occur.</span></span> <span data-ttu-id="f7ed6-113">Активация относится к вызовам любой из следующих функций активации:</span><span class="sxs-lookup"><span data-stu-id="f7ed6-113">Activation refers to calls to any of the following activation functions:</span></span>

-   [<span data-ttu-id="f7ed6-114">**кожетклассобжект**</span><span class="sxs-lookup"><span data-stu-id="f7ed6-114">**CoGetClassObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [<span data-ttu-id="f7ed6-115">**кокреатеинстанцеекс**</span><span class="sxs-lookup"><span data-stu-id="f7ed6-115">**CoCreateInstanceEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [<span data-ttu-id="f7ed6-116">**кожетинстанцефромфиле**</span><span class="sxs-lookup"><span data-stu-id="f7ed6-116">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [<span data-ttu-id="f7ed6-117">**кожетинстанцефромистораже**</span><span class="sxs-lookup"><span data-stu-id="f7ed6-117">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [<span data-ttu-id="f7ed6-118">**IMoniker:: Биндтубжект**</span><span class="sxs-lookup"><span data-stu-id="f7ed6-118">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

<span data-ttu-id="f7ed6-119">Чтобы запустить экземпляр заданного системой суррогата, установите значение **дллсуррогате** либо в пустую строку, либо в **null**.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-119">To launch an instance of the system-supplied surrogate, set the value of **DllSurrogate** either to an empty string or to **NULL**.</span></span> <span data-ttu-id="f7ed6-120">Чтобы указать запуск пользовательского суррогата, задайте в качестве значения путь к суррогату.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-120">To specify the launch of a custom surrogate, set the value to the path of the surrogate.</span></span>

<span data-ttu-id="f7ed6-121">Если для одного и того же AppID указаны оба [ремотесервернаме](remoteservername.md) и **Дллсуррогате** , значение **ремотесервернаме** игнорируется, а значение **дллсуррогате** вызывает активацию на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-121">If both [RemoteServerName](remoteservername.md) and **DllSurrogate** are specified for the same AppID, the **RemoteServerName** value is ignored and the **DllSurrogate** value causes an activation on the local computer.</span></span> <span data-ttu-id="f7ed6-122">Для удаленной суррогатной активации укажите **ремотесервернаме** , но не **дллсуррогате** на клиенте и укажите **дллсуррогате** на сервере.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-122">For remote surrogate activation, specify **RemoteServerName** but not **DllSurrogate** on the client, and specify **DllSurrogate** on the server.</span></span>

<span data-ttu-id="f7ed6-123">Сервер DLL, предназначенный для постоянного запуска в собственном суррогатном процессе, лучше настроить с AppID, равным его CLSID.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-123">A DLL server that is designed to always run alone in its own surrogate process is best configured with an AppID equal its CLSID.</span></span> <span data-ttu-id="f7ed6-124">В разделе **AppID** просто укажите **дллсуррогате** именованное значение с пустым строковым значением.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-124">Under **AppID**, simply specify a **DllSurrogate** named-value with an empty string value.</span></span>

<span data-ttu-id="f7ed6-125">Лучше всего настроить сервер DLL, предназначенный для работы в собственном суррогатном процессе, а также для обслуживания нескольких клиентов в сети с использованием значения [runas](runas.md) , указанного в разделе реестра **AppID** .</span><span class="sxs-lookup"><span data-stu-id="f7ed6-125">It is best to configure a DLL server that is designed to run alone in its own surrogate process and to service multiple clients across a network with a [RunAs](runas.md) value specified under the **AppID** registry key.</span></span> <span data-ttu-id="f7ed6-126">Указывает, определяет ли **runas** "Интерактивный пользователь" или конкретное удостоверение пользователя, зависит от пользовательского интерфейса, безопасности и других требований к серверу.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-126">Whether the **RunAs** specifies "Interactive User" or a specific user identity depends upon the user interface, security, and other server requirements.</span></span> <span data-ttu-id="f7ed6-127">Если указано значение **runas** , то для обслуживания всех клиентов загружается только один экземпляр сервера, независимо от удостоверения клиента.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-127">When a **RunAs** value is specified, only one instance of the server is loaded to service all of the clients, regardless of the identity of the client.</span></span> <span data-ttu-id="f7ed6-128">С другой стороны, не настраивайте сервер с помощью **runas** , если требуется, чтобы один экземпляр сервера DLL, выполняющийся в суррогате, выполнял обслуживание каждого удаленного клиента.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-128">On the other hand, do not configure the server with **RunAs** if the intention is to have one instance of the DLL server running in surrogate to service each remote client identity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7ed6-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f7ed6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7ed6-130">Требования к серверу DLL</span><span class="sxs-lookup"><span data-stu-id="f7ed6-130">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="f7ed6-131">Общий доступ к суррогатам</span><span class="sxs-lookup"><span data-stu-id="f7ed6-131">Surrogate Sharing</span></span>](surrogate-sharing.md)
</dt> </dl>

 

 