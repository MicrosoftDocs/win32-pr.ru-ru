---
description: ICE52 проверяет наличие закрытых свойств в таблице Аппсеарч. См. раздел о свойствах.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911908"
---
# <a name="ice52"></a><span data-ttu-id="efca8-104">ICE52</span><span class="sxs-lookup"><span data-stu-id="efca8-104">ICE52</span></span>

<span data-ttu-id="efca8-105">ICE52 проверяет наличие закрытых свойств в [таблице аппсеарч](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="efca8-105">ICE52 checks for private properties in the [AppSearch table](appsearch-table.md).</span></span> <span data-ttu-id="efca8-106">См. раздел [о свойствах](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="efca8-106">See [About Properties](about-properties.md).</span></span>

<span data-ttu-id="efca8-107">При использовании Windows 2000 все свойства, заданные в столбце свойств таблицы Аппсеарч, должны быть открытыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="efca8-107">When using Windows 2000 all properties set in the Property column of the AppSearch table must be public properties.</span></span>

## <a name="result"></a><span data-ttu-id="efca8-108">Результат</span><span class="sxs-lookup"><span data-stu-id="efca8-108">Result</span></span>

<span data-ttu-id="efca8-109">ICE52 отправляет предупреждение, если в таблице Аппсеарч есть закрытое свойство.</span><span class="sxs-lookup"><span data-stu-id="efca8-109">ICE52 posts a warning if there is a private property in the AppSearch table.</span></span>

## <a name="example"></a><span data-ttu-id="efca8-110">Пример</span><span class="sxs-lookup"><span data-stu-id="efca8-110">Example</span></span>

<span data-ttu-id="efca8-111">ICE52 отправляет следующее предупреждение для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="efca8-111">ICE52 posts the following warning for the example shown.</span></span>

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[<span data-ttu-id="efca8-112">Таблица Аппсеарч</span><span class="sxs-lookup"><span data-stu-id="efca8-112">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="efca8-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="efca8-113">Property</span></span>  | <span data-ttu-id="efca8-114">Подпись</span><span class="sxs-lookup"><span data-stu-id="efca8-114">Signature</span></span>  |
|-----------|------------|
| <span data-ttu-id="efca8-115">СВОЙСТВО1</span><span class="sxs-lookup"><span data-stu-id="efca8-115">PROPERTY1</span></span> | <span data-ttu-id="efca8-116">Signature1</span><span class="sxs-lookup"><span data-stu-id="efca8-116">Signature1</span></span> |
| <span data-ttu-id="efca8-117">Свойство2</span><span class="sxs-lookup"><span data-stu-id="efca8-117">Property2</span></span> | <span data-ttu-id="efca8-118">Signature2</span><span class="sxs-lookup"><span data-stu-id="efca8-118">Signature2</span></span> |



 

<span data-ttu-id="efca8-119">Чтобы устранить это предупреждение, измените пользовательское общедоступное свойство: СВОЙСТВО2.</span><span class="sxs-lookup"><span data-stu-id="efca8-119">To fix this warning change to the custom public property: PROPERTY2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efca8-120">См. также</span><span class="sxs-lookup"><span data-stu-id="efca8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efca8-121">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="efca8-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



