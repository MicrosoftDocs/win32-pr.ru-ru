---
title: API-интерфейс WinRM C++
description: Интерфейсы служба удаленного управления Windows могут использоваться для получения данных или управления ресурсами на удаленном компьютере. Этот API предназначен главным образом для внутреннего использования. Вместо этого рекомендуется использовать API-интерфейс оболочки клиента WinRM, если это возможно.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986634"
---
# <a name="winrm-c-api"></a><span data-ttu-id="49d2e-105">API-интерфейс WinRM C++</span><span class="sxs-lookup"><span data-stu-id="49d2e-105">WinRM C++ API</span></span>

<span data-ttu-id="49d2e-106">Интерфейсы служба удаленного управления Windows могут использоваться для получения данных или управления [*ресурсами*](windows-remote-management-glossary.md) на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="49d2e-106">The Windows Remote Management interfaces can be used to obtain data or manage [*resources*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="49d2e-107">Этот API предназначен главным образом для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="49d2e-107">This API is intended primarily for internal use.</span></span> <span data-ttu-id="49d2e-108">Вместо этого рекомендуется использовать [API-интерфейс оболочки клиента WinRM](client-shell-api.md) , если это возможно.</span><span class="sxs-lookup"><span data-stu-id="49d2e-108">We recommend using the [WinRM Client Shell API](client-shell-api.md) instead whenever possible.</span></span> <span data-ttu-id="49d2e-109">Интерфейсы в точности соответствуют API- [интерфейсу сценариев WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="49d2e-109">The interfaces closely correspond to the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="49d2e-110">Интерфейсы WinRM, которые наследуют непосредственно от **IDispatch** , имеют соответствующий объект скрипта.</span><span class="sxs-lookup"><span data-stu-id="49d2e-110">The WinRM interfaces that inherit directly from **IDispatch** each have a corresponding scripting object.</span></span> <span data-ttu-id="49d2e-111">Дополнительные сведения см. в разделе [API сценариев WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="49d2e-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="49d2e-112">Для многопоточных приложений WinRM не поддерживает отдельные потоки, обращающиеся к одному и тому же объекту [**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .</span><span class="sxs-lookup"><span data-stu-id="49d2e-112">For multithreaded applications, WinRM does not support separate threads accessing the same [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) object.</span></span>

<span data-ttu-id="49d2e-113">WinRM предоставляет следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="49d2e-113">The following interfaces are provided by WinRM.</span></span>

<dl> <dt>

<span data-ttu-id="49d2e-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="49d2e-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="49d2e-115">Предоставляет методы и свойства, используемые для создания нового сеанса и управления установленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="49d2e-115">Provides methods and properties used to create a new session and manage an established session.</span></span> <span data-ttu-id="49d2e-116">[**WSMan**](wsman.md) — это соответствующий объект скрипта.</span><span class="sxs-lookup"><span data-stu-id="49d2e-116">[**WSMan**](wsman.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="49d2e-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**ивсманекс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="49d2e-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="49d2e-118">Предоставляет методы и свойства, используемые для создания нового [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="49d2e-118">Provides methods and properties used to create a new [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span> <span data-ttu-id="49d2e-119">Этот метод доступен для объекта скрипта [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="49d2e-119">This method is available for the [**WSMan**](wsman.md) scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="49d2e-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**ивсманконнектионоптионс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span><span class="sxs-lookup"><span data-stu-id="49d2e-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span></span>
</dt> <dd>

<span data-ttu-id="49d2e-121">Определяет имя пользователя и пароль, используемые для удаленных соединений.</span><span class="sxs-lookup"><span data-stu-id="49d2e-121">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="49d2e-122">[**ConnectionOptions**](connectionoptions.md) — это соответствующий объект скрипта.</span><span class="sxs-lookup"><span data-stu-id="49d2e-122">[**ConnectionOptions**](connectionoptions.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="49d2e-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="49d2e-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span></span>
</dt> <dd>

<span data-ttu-id="49d2e-124">Определяет сетевые операции и свойства, доступные для сеанса.</span><span class="sxs-lookup"><span data-stu-id="49d2e-124">Defines the network operations and properties available for the session.</span></span> <span data-ttu-id="49d2e-125">[**Session**](session.md) — это соответствующий объект скрипта.</span><span class="sxs-lookup"><span data-stu-id="49d2e-125">[**Session**](session.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="49d2e-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**ивсманенумератор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span><span class="sxs-lookup"><span data-stu-id="49d2e-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span></span>
</dt> <dd>

<span data-ttu-id="49d2e-127">Представляет коллекцию результатов, возвращенных при перечислении ресурса.</span><span class="sxs-lookup"><span data-stu-id="49d2e-127">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="49d2e-128">[**Перечислитель**](enumerator.md) — это соответствующий объект скрипта.</span><span class="sxs-lookup"><span data-stu-id="49d2e-128">[**Enumerator**](enumerator.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="49d2e-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="49d2e-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span></span>
</dt> <dd>

<span data-ttu-id="49d2e-130">Предоставляет путь к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="49d2e-130">Supplies the path to a resource.</span></span> <span data-ttu-id="49d2e-131">Вы можете использовать объект [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) вместо [*URI ресурса*](windows-remote-management-glossary.md) в операциях с объектами [**сеанса**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="49d2e-131">You can use an [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="49d2e-132">[**ResourceLocator**](resourcelocator.md) — это соответствующий объект скрипта.</span><span class="sxs-lookup"><span data-stu-id="49d2e-132">[**ResourceLocator**](resourcelocator.md) is the corresponding scripting object.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="49d2e-133">См. также</span><span class="sxs-lookup"><span data-stu-id="49d2e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49d2e-134">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="49d2e-134">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




