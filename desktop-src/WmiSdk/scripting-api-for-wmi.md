---
description: Справочник по скриптам WMI содержит определения для API сценариев WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API сценариев для инструментария WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898566"
---
# <a name="scripting-api-for-wmi"></a><span data-ttu-id="a02ab-103">API сценариев для инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="a02ab-103">Scripting API for WMI</span></span>

<span data-ttu-id="a02ab-104">Справочник по скриптам WMI содержит определения для API сценариев WMI.</span><span class="sxs-lookup"><span data-stu-id="a02ab-104">The WMI scripting reference contains definitions for the WMI Scripting API.</span></span> <span data-ttu-id="a02ab-105">Используйте этот API при написании приложений с помощью Microsoft Visual Basic, Visual Basic для приложений, Visual Basic Scripting Edition (VBScript) или любого другого языка сценариев, поддерживающего активные технологии сценариев.</span><span class="sxs-lookup"><span data-stu-id="a02ab-105">Use this API if writing applications with Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript), or any other scripting language that supports active scripting technologies.</span></span>

> [!Note]  
> <span data-ttu-id="a02ab-106">PowerShell также доступен для создания сценариев с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="a02ab-106">PowerShell is also available for scripting with WMI.</span></span> <span data-ttu-id="a02ab-107">Командлет Get-WMI и три типа ускорителей ( \[ WMI \] , \[ WMICLASS \] и \[ вмисеарчер \] ) обеспечивают базовый административный доступ к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="a02ab-107">The Get-WMI cmdlet and the three type accelerators (\[wmi\], \[wmiclass\], and \[wmisearcher\]) enable basic administrative access to WMI.</span></span> <span data-ttu-id="a02ab-108">Дополнительные сведения см. [в разделе Создание сценариев с помощью Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="a02ab-108">For more information, see [Scripting with Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span></span>

 

<span data-ttu-id="a02ab-109">Объекты сценариев WMI, за исключением [**SWbemDateTime**](swbemdatetime.md) , не помечены как "надежные" для сценариев, выполняющихся на HTML-страницах в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a02ab-109">WMI scripting objects, except for [**SWbemDateTime**](swbemdatetime.md) are not marked safe for scripting for scripts running on HTML pages in Internet Explorer.</span></span> <span data-ttu-id="a02ab-110">Таким образом, если уровень безопасности в Internet Explorer не будет сокращен, сценарий завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a02ab-110">Therefore, unless the security level within Internet Explorer is lowered, the script will fail.</span></span> <span data-ttu-id="a02ab-111">**SWbemDateTime** помечен как надежный для инициализации и создания сценариев.</span><span class="sxs-lookup"><span data-stu-id="a02ab-111">**SWbemDateTime** is marked safe for initialization and scripting.</span></span> <span data-ttu-id="a02ab-112">Тем не менее, используйте все объекты сценариев WMI в вызовах **GetObject** и **CreateObject** для кода на стороне сервера в Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="a02ab-112">However, use all WMI scripting objects in **GetObject** and **CreateObject** calls on server-side code in Active Server Pages (ASP).</span></span>

-   [<span data-ttu-id="a02ab-113">Объектная модель API сценариев</span><span class="sxs-lookup"><span data-stu-id="a02ab-113">Scripting API Object Model</span></span>](scripting-api-object-model.md)
-   [<span data-ttu-id="a02ab-114">Соглашения о документе для API скриптов</span><span class="sxs-lookup"><span data-stu-id="a02ab-114">Document Conventions for the Scripting API</span></span>](document-conventions-for-the-scripting-api.md)
-   [<span data-ttu-id="a02ab-115">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="a02ab-115">Scripting API Objects</span></span>](scripting-api-objects.md)
-   [<span data-ttu-id="a02ab-116">Константы API скриптов</span><span class="sxs-lookup"><span data-stu-id="a02ab-116">Scripting API Constants</span></span>](scripting-api-constants.md)

## <a name="related-topics"></a><span data-ttu-id="a02ab-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a02ab-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a02ab-118">Справочник по инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="a02ab-118">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="a02ab-119">Коды возврата WMI</span><span class="sxs-lookup"><span data-stu-id="a02ab-119">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

 



