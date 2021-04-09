---
description: ICE15 проверяет, что тип содержимого и ссылки на расширения в таблицах MIME и расширений являются обратными. Таблица MIME должна ссылаться на тип содержимого на расширение, которое таблица расширений ссылается на тот же тип содержимого.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081067"
---
# <a name="ice15"></a><span data-ttu-id="c56da-104">ICE15</span><span class="sxs-lookup"><span data-stu-id="c56da-104">ICE15</span></span>

<span data-ttu-id="c56da-105">ICE15 проверяет, что тип содержимого и ссылки на расширения в таблицах [MIME](mime-table.md) и [расширений](extension-table.md) являются обратными.</span><span class="sxs-lookup"><span data-stu-id="c56da-105">ICE15 validates that content type and extension references in the [MIME](mime-table.md) and [Extension](extension-table.md) tables are reciprocal.</span></span> <span data-ttu-id="c56da-106">Таблица MIME должна ссылаться на тип содержимого на расширение, которое таблица расширений ссылается на тот же тип содержимого.</span><span class="sxs-lookup"><span data-stu-id="c56da-106">The MIME table must reference a content type to an extension that the Extension table references back to the same content type.</span></span>

<span data-ttu-id="c56da-107">Несколько расширений могут ссылаться на один и тот же тип MIME, если тип MIME ссылается на одно из расширений.</span><span class="sxs-lookup"><span data-stu-id="c56da-107">Multiple extensions can reference the same MIME type, as long as the MIME type references back to one of the extensions.</span></span> <span data-ttu-id="c56da-108">Несколько типов MIME могут ссылаться на одно и то же расширение, если расширение ссылается на один из типов MIME.</span><span class="sxs-lookup"><span data-stu-id="c56da-108">Multiple MIME types can reference the same extension, as long as the extension references back to one of the MIME types.</span></span>

<span data-ttu-id="c56da-109">Обратите внимание, что всякий раз, когда MIME ссылается на расширение, это расширение не может иметь \_ столбец MIME в таблице Extension со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="c56da-109">Note that whenever a MIME references an extension, that extension cannot have the MIME\_ column in the Extension table set to Null.</span></span>

## <a name="result"></a><span data-ttu-id="c56da-110">Результат</span><span class="sxs-lookup"><span data-stu-id="c56da-110">Result</span></span>

<span data-ttu-id="c56da-111">ICE15 отправляет сообщение об ошибке, если тип содержимого и ссылки на расширение не являются обратными.</span><span class="sxs-lookup"><span data-stu-id="c56da-111">ICE15 posts an error if the content type and extension references are not reciprocal.</span></span>

## <a name="example"></a><span data-ttu-id="c56da-112">Пример</span><span class="sxs-lookup"><span data-stu-id="c56da-112">Example</span></span>

<span data-ttu-id="c56da-113">ICE15 отправляет два сообщения об ошибке для приведенного примера:</span><span class="sxs-lookup"><span data-stu-id="c56da-113">ICE15 posts two error messages for the example shown:</span></span>

-   <span data-ttu-id="c56da-114">Типы содержимого Test/x-закрыли в таблице MIME ссылаются на расширение TST, но расширение TST в таблице расширений ссылается на закрылки/x-колыханий.</span><span class="sxs-lookup"><span data-stu-id="c56da-114">The content type test/x-flaps in the MIME table references the extension tst, but the extension tst in the Extension table references flaps/x-flaps.</span></span> <span data-ttu-id="c56da-115">Это не является обратным.</span><span class="sxs-lookup"><span data-stu-id="c56da-115">This is not reciprocal.</span></span>
-   <span data-ttu-id="c56da-116">Закрылки типа содержимого ссылается на расширение FLP, но это расширение содержит запись NULL в \_ СТОЛБЦЕ MIME таблицы Extension.</span><span class="sxs-lookup"><span data-stu-id="c56da-116">The content type flaps/x-flaps references the extension flp, but that extension has a Null entry in the MIME\_ column of the Extension table.</span></span>

<span data-ttu-id="c56da-117">[Таблица MIME](mime-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="c56da-117">[MIME Table](mime-table.md) (partial)</span></span>



| <span data-ttu-id="c56da-118">ContentType</span><span class="sxs-lookup"><span data-stu-id="c56da-118">ContentType</span></span>   | <span data-ttu-id="c56da-119">Расширение\_</span><span class="sxs-lookup"><span data-stu-id="c56da-119">Extension\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="c56da-120">тест/x-тест</span><span class="sxs-lookup"><span data-stu-id="c56da-120">test/x-test</span></span>   | <span data-ttu-id="c56da-121">TST</span><span class="sxs-lookup"><span data-stu-id="c56da-121">tst</span></span>         |
| <span data-ttu-id="c56da-122">закрылки/x</span><span class="sxs-lookup"><span data-stu-id="c56da-122">flaps/x-flaps</span></span> | <span data-ttu-id="c56da-123">FLP</span><span class="sxs-lookup"><span data-stu-id="c56da-123">flp</span></span>         |



 

<span data-ttu-id="c56da-124">[Таблица расширения](extension-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="c56da-124">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="c56da-125">Расширение</span><span class="sxs-lookup"><span data-stu-id="c56da-125">Extension</span></span> | <span data-ttu-id="c56da-126">MIME\_</span><span class="sxs-lookup"><span data-stu-id="c56da-126">MIME\_</span></span>        |
|-----------|---------------|
| <span data-ttu-id="c56da-127">TST</span><span class="sxs-lookup"><span data-stu-id="c56da-127">tst</span></span>       | <span data-ttu-id="c56da-128">закрылки/x</span><span class="sxs-lookup"><span data-stu-id="c56da-128">flaps/x-flaps</span></span> |
| <span data-ttu-id="c56da-129">FLP</span><span class="sxs-lookup"><span data-stu-id="c56da-129">flp</span></span>       | <span data-ttu-id="c56da-130">NULL</span><span class="sxs-lookup"><span data-stu-id="c56da-130">Null</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="c56da-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c56da-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c56da-132">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c56da-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



