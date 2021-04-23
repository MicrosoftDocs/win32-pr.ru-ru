---
description: ICE11 используется с параллельными установками. Параллельные установки не рекомендуются для установки приложений, предназначенных для выпуска в общедоступной версии. Сведения о параллельных установках см. в разделе одновременная установка.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998801"
---
# <a name="ice11"></a><span data-ttu-id="b0b19-105">ICE11</span><span class="sxs-lookup"><span data-stu-id="b0b19-105">ICE11</span></span>

<span data-ttu-id="b0b19-106">ICE11 используется с параллельными установками.</span><span class="sxs-lookup"><span data-stu-id="b0b19-106">The ICE11 is used with concurrent installations.</span></span> <span data-ttu-id="b0b19-107">Параллельные установки не рекомендуются для установки приложений, предназначенных для выпуска в общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="b0b19-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="b0b19-108">Сведения о параллельных установках см. в разделе [одновременная установка](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="b0b19-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

## <a name="result"></a><span data-ttu-id="b0b19-109">Результат</span><span class="sxs-lookup"><span data-stu-id="b0b19-109">Result</span></span>

<span data-ttu-id="b0b19-110">ICE11 проверяет исходный столбец в [таблице CustomAction](customaction-table.md) для одновременных настраиваемых действий установки.</span><span class="sxs-lookup"><span data-stu-id="b0b19-110">ICE11 validates the Source column of the [CustomAction table](customaction-table.md) of concurrent installation custom actions.</span></span> <span data-ttu-id="b0b19-111">Исходный столбец должен содержать допустимый [GUID](guid.md) (код продукта MSI).</span><span class="sxs-lookup"><span data-stu-id="b0b19-111">The Source column must contain a valid [GUID](guid.md) (MSI product code).</span></span>

<span data-ttu-id="b0b19-112">ICE11 отправляет сообщение об ошибке, если исходный столбец таблицы CustomAction создан неправильно для одновременных настраиваемых действий установки.</span><span class="sxs-lookup"><span data-stu-id="b0b19-112">ICE11 posts an error if the Source column of the CustomAction table is authored incorrectly for concurrent installation custom actions.</span></span>

## <a name="example"></a><span data-ttu-id="b0b19-113">Пример</span><span class="sxs-lookup"><span data-stu-id="b0b19-113">Example</span></span>

<span data-ttu-id="b0b19-114">ICE отправляет следующие сообщения об ошибках для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="b0b19-114">ICE posts the following error messages for the example shown.</span></span>

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

<span data-ttu-id="b0b19-115">[Таблица свойств](property-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="b0b19-115">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="b0b19-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="b0b19-116">Property</span></span>        | <span data-ttu-id="b0b19-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b0b19-117">Value</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="b0b19-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="b0b19-118">**ProductCode**</span></span> | <span data-ttu-id="b0b19-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="b0b19-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |



 

<span data-ttu-id="b0b19-120">[Таблица CustomAction](customaction-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="b0b19-120">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="b0b19-121">CustomAction</span><span class="sxs-lookup"><span data-stu-id="b0b19-121">CustomAction</span></span> | <span data-ttu-id="b0b19-122">Тип</span><span class="sxs-lookup"><span data-stu-id="b0b19-122">Type</span></span> | <span data-ttu-id="b0b19-123">Источник</span><span class="sxs-lookup"><span data-stu-id="b0b19-123">Source</span></span>                                 |
|--------------|------|----------------------------------------|
| <span data-ttu-id="b0b19-124">CA1</span><span class="sxs-lookup"><span data-stu-id="b0b19-124">CA1</span></span>          | <span data-ttu-id="b0b19-125">39</span><span class="sxs-lookup"><span data-stu-id="b0b19-125">39</span></span>   | <span data-ttu-id="b0b19-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="b0b19-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |
| <span data-ttu-id="b0b19-127">CA2</span><span class="sxs-lookup"><span data-stu-id="b0b19-127">CA2</span></span>          | <span data-ttu-id="b0b19-128">39</span><span class="sxs-lookup"><span data-stu-id="b0b19-128">39</span></span>   | <span data-ttu-id="b0b19-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="b0b19-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span></span> |
| <span data-ttu-id="b0b19-130">CA3</span><span class="sxs-lookup"><span data-stu-id="b0b19-130">CA3</span></span>          | <span data-ttu-id="b0b19-131">39</span><span class="sxs-lookup"><span data-stu-id="b0b19-131">39</span></span>   | <span data-ttu-id="b0b19-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="b0b19-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span></span> |
| <span data-ttu-id="b0b19-133">CA4</span><span class="sxs-lookup"><span data-stu-id="b0b19-133">CA4</span></span>          | <span data-ttu-id="b0b19-134">39</span><span class="sxs-lookup"><span data-stu-id="b0b19-134">39</span></span>   | <span data-ttu-id="b0b19-135">ProductCode</span><span class="sxs-lookup"><span data-stu-id="b0b19-135">ProductCode</span></span>                            |



 

<span data-ttu-id="b0b19-136">Чтобы устранить ошибки, для CA1 нельзя выполнить параллельную установку "базового пакета".</span><span class="sxs-lookup"><span data-stu-id="b0b19-136">To fix the errors, for CA1, you cannot do a concurrent installation of the "base package".</span></span> <span data-ttu-id="b0b19-137">Это приведет к рекурсивной установке.</span><span class="sxs-lookup"><span data-stu-id="b0b19-137">This would result in a recursive installation.</span></span> <span data-ttu-id="b0b19-138">Эта запись должна быть удалена, либо исходный столбец должен быть изменен на GUID объявленного MSI, который отличается от GUID основного пакета.</span><span class="sxs-lookup"><span data-stu-id="b0b19-138">This entry should be removed or the Source column should be changed to a GUID for an advertised MSI that differs from the base package's GUID.</span></span> <span data-ttu-id="b0b19-139">Для CA2 все символы в верхнем регистре GUID.</span><span class="sxs-lookup"><span data-stu-id="b0b19-139">For CA2, make all characters of the GUID uppercase.</span></span> <span data-ttu-id="b0b19-140">Наконец, измените исходный столбец CA4's, чтобы он ссылался на допустимый идентификатор GUID объявленного MSI.</span><span class="sxs-lookup"><span data-stu-id="b0b19-140">Lastly, change CA4's Source column to reference a valid GUID of an advertised MSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0b19-141">См. также</span><span class="sxs-lookup"><span data-stu-id="b0b19-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b19-142">Параллельные установки</span><span class="sxs-lookup"><span data-stu-id="b0b19-142">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="b0b19-143">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="b0b19-143">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



