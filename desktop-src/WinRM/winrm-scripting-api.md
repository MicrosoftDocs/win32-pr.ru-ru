---
title: API сценариев WinRM
description: Служба удаленного управления Windows объекты скрипта реализуются как уровень выше протокола WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700639"
---
# <a name="winrm-scripting-api"></a><span data-ttu-id="fc896-103">API сценариев WinRM</span><span class="sxs-lookup"><span data-stu-id="fc896-103">WinRM Scripting API</span></span>

<span data-ttu-id="fc896-104">Служба удаленного управления Windows объекты скрипта реализуются как слой над [протокол WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="fc896-104">Windows Remote Management scripting objects are implemented as a layer above the [WS-Management Protocol](ws-management-protocol.md).</span></span> <span data-ttu-id="fc896-105">Объекты скрипта позволяют получать данные или управлять [*ресурсами*](windows-remote-management-glossary.md) на локальных и удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="fc896-105">The scripting objects enable you to obtain data or manage [*resources*](windows-remote-management-glossary.md) on local and remote computers.</span></span>

## <a name="ws-management-objects"></a><span data-ttu-id="fc896-106">WS-Management объекты</span><span class="sxs-lookup"><span data-stu-id="fc896-106">WS-Management Objects</span></span>

<span data-ttu-id="fc896-107">Каждый объект скрипта имеет соответствующий интерфейс C++.</span><span class="sxs-lookup"><span data-stu-id="fc896-107">Each scripting object has a corresponding C++ interface.</span></span> <span data-ttu-id="fc896-108">Дополнительные сведения см. в разделе [WinRM C++ API](winrm-c---api.md) и [сценарии в Служба удаленного управления Windows](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="fc896-108">For more information, see [WinRM C++ API](winrm-c---api.md) and [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="fc896-109">В API-интерфейсах сценариев WinRM предоставляются следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="fc896-109">The following objects are provided by the WinRM Scripting API.</span></span>

<dl> <dt>

<span data-ttu-id="fc896-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span><span class="sxs-lookup"><span data-stu-id="fc896-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span></span>
</dt> <dd>

<span data-ttu-id="fc896-111">Определяет имя пользователя и пароль, используемые для удаленных соединений.</span><span class="sxs-lookup"><span data-stu-id="fc896-111">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="fc896-112">Имя пользователя и пароль передаются при вызове метода [**креатеконнектионоптионс**](wsman-createconnectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="fc896-112">The user name and password are passed when calling the [**CreateConnectionOptions**](wsman-createconnectionoptions.md) method.</span></span> <span data-ttu-id="fc896-113">Дополнительные сведения см. в разделе [Получение данных с удаленного компьютера](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fc896-113">For more information, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="fc896-114">Соответствующий интерфейс C++ — [**ивсманконнектионоптионс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span><span class="sxs-lookup"><span data-stu-id="fc896-114">The corresponding C++ interface is [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span></span>

</dd> <dt>

<span data-ttu-id="fc896-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Перечислитель**](enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="fc896-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)</span></span>
</dt> <dd>

<span data-ttu-id="fc896-116">Представляет коллекцию результатов, возвращенных при перечислении ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc896-116">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="fc896-117">Дополнительные сведения см. [в разделе перечисление или вывод всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="fc896-117">For more information, see [Enumerating or Listing All the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span> <span data-ttu-id="fc896-118">Соответствующий интерфейс C++ — [**ивсманенумератор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="fc896-118">The corresponding C++ interface is [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="fc896-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span><span class="sxs-lookup"><span data-stu-id="fc896-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span></span>
</dt> <dd>

<span data-ttu-id="fc896-120">Предоставляет путь к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="fc896-120">Supplies the path to a resource.</span></span> <span data-ttu-id="fc896-121">Вместо [*URI ресурса*](windows-remote-management-glossary.md) в операциях объекта [**сеанса**](session.md) можно использовать объект [**ResourceLocator**](resourcelocator.md) , например [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="fc896-121">You can use a [**ResourceLocator**](resourcelocator.md) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations, such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="fc896-122">Соответствующий интерфейс C++ — [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="fc896-122">The corresponding C++ interface is [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span>

</dd> <dt>

<span data-ttu-id="fc896-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Сессии**](session.md)</span><span class="sxs-lookup"><span data-stu-id="fc896-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)</span></span>
</dt> <dd>

<span data-ttu-id="fc896-124">Определяет сетевые операции и свойства, доступные для сеанса, такие как [**сеанс. Get**](session-get.md), [**сеанс. Перечисление**](session-enumerate.md), [**сеанс. Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="fc896-124">Defines the network operations and properties available for the session, such as [**Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md).</span></span> <span data-ttu-id="fc896-125">Дополнительные сведения см. [в разделе Получение данных с локального компьютера](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fc896-125">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span> <span data-ttu-id="fc896-126">Соответствующий интерфейс C++ — [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span><span class="sxs-lookup"><span data-stu-id="fc896-126">The corresponding C++ interface is [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span></span>

</dd> <dt>

<span data-ttu-id="fc896-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**Ведущий**](wsman.md)</span><span class="sxs-lookup"><span data-stu-id="fc896-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span></span>
</dt> <dd>

<span data-ttu-id="fc896-128">Предоставляет методы и свойства, используемые для создания нового сеанса или управления установленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="fc896-128">Provides methods and properties used to create a new session or manage an established session.</span></span> <span data-ttu-id="fc896-129">Дополнительные сведения см. в разделе [использование служба удаленного управления Windows](using-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="fc896-129">For more information see, [Using Windows Remote Management](using-windows-remote-management.md).</span></span> <span data-ttu-id="fc896-130">Соответствующими интерфейсами C++ являются [**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) и [**ивсманекс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span><span class="sxs-lookup"><span data-stu-id="fc896-130">The corresponding C++ interfaces are [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="fc896-131">См. также</span><span class="sxs-lookup"><span data-stu-id="fc896-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc896-132">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="fc896-132">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fc896-133">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="fc896-133">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fc896-134">Создание сценариев в служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="fc896-134">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fc896-135">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="fc896-135">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




