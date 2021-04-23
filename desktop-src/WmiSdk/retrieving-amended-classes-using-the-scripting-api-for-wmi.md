---
description: Если вы используете API скриптов для инструментария WMI для получения или хранения сведений о локализованном классе, укажите языковой стандарт как часть моникера.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Получение измененных классов с помощью API скриптов для WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701998"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a><span data-ttu-id="069d4-103">Получение измененных классов с помощью API скриптов для WMI</span><span class="sxs-lookup"><span data-stu-id="069d4-103">Retrieving Amended Classes Using the Scripting API for WMI</span></span>

<span data-ttu-id="069d4-104">Если вы используете API скриптов для инструментария WMI для получения или хранения сведений о локализованном классе, укажите языковой стандарт как часть моникера.</span><span class="sxs-lookup"><span data-stu-id="069d4-104">If you are using the Scripting API for WMI to retrieve or store localized class information, specify the locale as part of a moniker.</span></span> <span data-ttu-id="069d4-105">Также можно указать имя локали в параметре *стрлокале* для метода [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="069d4-105">Or, you can supply the locale name in the *strLocale* parameter to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span> <span data-ttu-id="069d4-106">При чтении или записи измененных классов укажите, что необходимо использовать локализованные определения классов, указав [вбемфлагусеамендедкуалифиерс](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) в качестве флага для параметра *ифлагс* вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="069d4-106">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) as a flag for the *iFlags* parameter of the method you call.</span></span> <span data-ttu-id="069d4-107">Для указания языкового стандарта PowerShell можно использовать параметр *-locale* в командлете [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="069d4-107">For PowerShell, you can use the *-locale* parameter on [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) to specify the locale.</span></span>

<span data-ttu-id="069d4-108">В следующем примере кода показано, как получить локализованный класс с помощью моникера скрипта WMI или параметра-Locale.</span><span class="sxs-lookup"><span data-stu-id="069d4-108">The following code example shows how to retrieve a localized class by using a WMI scripting moniker or the -locale parameter.</span></span>


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





<span data-ttu-id="069d4-109">В следующем примере кода показано, как задать параметр locale и использовать флаг [вбемфлагусеамендедкуалифиерс](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="069d4-109">The following code example shows how to set the locale parameter and use the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> <span data-ttu-id="069d4-110">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="069d4-110">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="069d4-111">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="069d4-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="069d4-112">В следующей таблице перечислены методы, принимающие флаг [вбемфлагусеамендедкуалифиерс](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="069d4-112">The following table lists the methods that accept the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>



| <span data-ttu-id="069d4-113">Синхронный метод</span><span class="sxs-lookup"><span data-stu-id="069d4-113">Synchronous Method</span></span>                                                 | <span data-ttu-id="069d4-114">Асинхронный метод</span><span class="sxs-lookup"><span data-stu-id="069d4-114">Asynchronous Method</span></span>                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="069d4-115">**SWbemServices. Субклассесоф**</span><span class="sxs-lookup"><span data-stu-id="069d4-115">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)   | [<span data-ttu-id="069d4-116">**SWbemServices. Субклассесофасинк**</span><span class="sxs-lookup"><span data-stu-id="069d4-116">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)   |
| [<span data-ttu-id="069d4-117">**SWbemObject. подклассы\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-117">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)        | [<span data-ttu-id="069d4-118">**SWbemObject. Субклассесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-118">**SWbemObject.SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)        |
| [<span data-ttu-id="069d4-119">**SWbemServices. Инстанцесоф**</span><span class="sxs-lookup"><span data-stu-id="069d4-119">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)     | [<span data-ttu-id="069d4-120">**SWbemServices. Инстанцесофасинк**</span><span class="sxs-lookup"><span data-stu-id="069d4-120">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)     |
| [<span data-ttu-id="069d4-121">**SWbemObject. Instances\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-121">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)          | [<span data-ttu-id="069d4-122">**SWbemObject. Инстанцесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-122">**SWbemObject.InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)          |
| [<span data-ttu-id="069d4-123">**SWbemServices.ExeКкуери**</span><span class="sxs-lookup"><span data-stu-id="069d4-123">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)         | [<span data-ttu-id="069d4-124">**SWbemServices.ExeКкуерясинк**</span><span class="sxs-lookup"><span data-stu-id="069d4-124">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)         |
| [<span data-ttu-id="069d4-125">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="069d4-125">**SWbemServices.Get**</span></span>](swbemservices-get.md)                     | [<span data-ttu-id="069d4-126">**SWbemServices. Async**</span><span class="sxs-lookup"><span data-stu-id="069d4-126">**SWbemServices.GetAsync**</span></span>](swbemservices-getasync.md)                     |
| [<span data-ttu-id="069d4-127">**SWbemObject. размещение\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-127">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)                      | [<span data-ttu-id="069d4-128">**SWbemObject. Путасинк\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-128">**SWbemObject.PutAsync\_**</span></span>](swbemobject-putasync-.md)                      |
| [<span data-ttu-id="069d4-129">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="069d4-129">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)   | [<span data-ttu-id="069d4-130">**SWbemServices. Референцестоасинк**</span><span class="sxs-lookup"><span data-stu-id="069d4-130">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)   |
| [<span data-ttu-id="069d4-131">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-131">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)        | [<span data-ttu-id="069d4-132">**SWbemObject. Референцесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-132">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)        |
| [<span data-ttu-id="069d4-133">**SWbemServices. АссоЦиаторсоф**</span><span class="sxs-lookup"><span data-stu-id="069d4-133">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md) | [<span data-ttu-id="069d4-134">**SWbemServices. АссоЦиаторсофасинк**</span><span class="sxs-lookup"><span data-stu-id="069d4-134">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md) |
| [<span data-ttu-id="069d4-135">**SWbemObject. соединители\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-135">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)      | [<span data-ttu-id="069d4-136">**SWbemObject. АссоЦиаторсасинк\_**</span><span class="sxs-lookup"><span data-stu-id="069d4-136">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)      |



 

 

 
