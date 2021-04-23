---
description: 'ICE05 проверяет, что определенные таблицы содержат необходимые записи. Это включает, но не ограничивается проверкой таблицы свойств на наличие обязательных свойств: ProductName, Продуктлангуаже, ProductVersion, ProductCode и manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650935"
---
# <a name="ice05"></a><span data-ttu-id="38381-104">ICE05</span><span class="sxs-lookup"><span data-stu-id="38381-104">ICE05</span></span>

<span data-ttu-id="38381-105">ICE05 проверяет, что определенные таблицы содержат необходимые записи.</span><span class="sxs-lookup"><span data-stu-id="38381-105">ICE05 validates that certain tables contain required entries.</span></span> <span data-ttu-id="38381-106">Это включает, но не ограничивается проверкой [таблицы свойств](property-table.md) на наличие обязательных свойств: [**ProductName**](productname.md), [**продуктлангуаже**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)и [**Manufacturer**](manufacturer.md).</span><span class="sxs-lookup"><span data-stu-id="38381-106">This includes, but is not restricted to, checking the [Property table](property-table.md) for the required properties: [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md), and [**Manufacturer**](manufacturer.md).</span></span>

## <a name="result"></a><span data-ttu-id="38381-107">Результат</span><span class="sxs-lookup"><span data-stu-id="38381-107">Result</span></span>

<span data-ttu-id="38381-108">ICE05 отправляет сообщение об ошибке, если требуемая запись отсутствует.</span><span class="sxs-lookup"><span data-stu-id="38381-108">ICE05 posts an error if a required entry is missing.</span></span>

## <a name="example"></a><span data-ttu-id="38381-109">Пример</span><span class="sxs-lookup"><span data-stu-id="38381-109">Example</span></span>

<span data-ttu-id="38381-110">В приведенном примере ICE05 сообщит, что запись "ProductVersion" является обязательной в таблице "Property".</span><span class="sxs-lookup"><span data-stu-id="38381-110">For the example shown, ICE05 would report that the entry: 'ProductVersion' is required in the 'Property' table.</span></span>

<span data-ttu-id="38381-111">[Таблица свойств](property-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="38381-111">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="38381-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="38381-112">Property</span></span>                           | <span data-ttu-id="38381-113">Значение</span><span class="sxs-lookup"><span data-stu-id="38381-113">Value</span></span>     |
|------------------------------------|-----------|
| [<span data-ttu-id="38381-114">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="38381-114">**ProductName**</span></span>](productname.md) | <span data-ttu-id="38381-115">мипродукт</span><span class="sxs-lookup"><span data-stu-id="38381-115">MyProduct</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="38381-116">См. также</span><span class="sxs-lookup"><span data-stu-id="38381-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38381-117">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="38381-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



