---
description: ICE14 проверяет таблицу компонентов базы данных установщик Windows.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346325"
---
# <a name="ice14"></a><span data-ttu-id="03215-103">ICE14</span><span class="sxs-lookup"><span data-stu-id="03215-103">ICE14</span></span>

<span data-ttu-id="03215-104">ICE14 проверяет следующие компоненты на предмет:</span><span class="sxs-lookup"><span data-stu-id="03215-104">ICE14 validates the following for features:</span></span>

-   <span data-ttu-id="03215-105">У корневых родительских функций нет бита Мсидбфеатуреаттрибутесфолловпарент, установленного в столбце Attributes [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="03215-105">That root parent features do not have the msidbFeatureAttributesFollowParent bit set in the Attributes column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="03215-106">У корневого компонента нет родителя.</span><span class="sxs-lookup"><span data-stu-id="03215-106">A root feature does not have a parent.</span></span>
-   <span data-ttu-id="03215-107">Функция не имеет такой же записи в \_ родительских столбцах функций и компонентов [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="03215-107">That no feature has the same entry in the Feature and Feature\_Parent columns of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="03215-108">Ни одна из функций не может быть ее родителем.</span><span class="sxs-lookup"><span data-stu-id="03215-108">No feature can be its own parent.</span></span>

## <a name="result"></a><span data-ttu-id="03215-109">Результат</span><span class="sxs-lookup"><span data-stu-id="03215-109">Result</span></span>

<span data-ttu-id="03215-110">ICE14 отправляет сообщение об ошибке, если обнаруживает корневую функцию с установленным битом Мсидбфеатуреаттрибутесфолловпарент или функцию с идентичными записями в \_ родительских столбцах функции и компонента в таблице Feature.</span><span class="sxs-lookup"><span data-stu-id="03215-110">ICE14 posts an error message if it finds a root feature with the msidbFeatureAttributesFollowParent bit set or a feature with identical entries in the Feature and Feature\_Parent columns of the Feature table.</span></span>

## <a name="example"></a><span data-ttu-id="03215-111">Пример</span><span class="sxs-lookup"><span data-stu-id="03215-111">Example</span></span>

<span data-ttu-id="03215-112">ICE14 возвращает следующие ошибки в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="03215-112">ICE14 would return the following errors for the following example:</span></span>

-   <span data-ttu-id="03215-113">Функция «спорт» имеет то же значение в родительских столбцах «компонент» и «функция» \_ таблицы File.</span><span class="sxs-lookup"><span data-stu-id="03215-113">The feature Sport has the same value in the Feature and Feature\_Parent columns of the File table.</span></span>
-   <span data-ttu-id="03215-114">В корневом компоненте "Спорт" установлен бит Мсидбфеатуреаттрибутесфолловпарент.</span><span class="sxs-lookup"><span data-stu-id="03215-114">The root feature Sport has the msidbFeatureAttributesFollowParent bit set.</span></span>

<span data-ttu-id="03215-115">В дереве функций этого примера «спорт» является корневой функцией и родителем функций Swimming и футбола.</span><span class="sxs-lookup"><span data-stu-id="03215-115">In the feature tree of this example, Sport is the root feature and a parent of the Swimming and Football features.</span></span> <span data-ttu-id="03215-116">Freestyle — это дочерняя функция Swimming.</span><span class="sxs-lookup"><span data-stu-id="03215-116">Freestyle is a child feature of Swimming.</span></span> <span data-ttu-id="03215-117">Таучфутбалл — это дочерняя функция футбольной футболки.</span><span class="sxs-lookup"><span data-stu-id="03215-117">TouchFootball is a child feature of Football.</span></span>

<span data-ttu-id="03215-118">[Таблица компонентов](feature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="03215-118">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="03215-119">Функция</span><span class="sxs-lookup"><span data-stu-id="03215-119">Feature</span></span>       | <span data-ttu-id="03215-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="03215-120">Attributes</span></span> | <span data-ttu-id="03215-121">\_Родительский компонент функции</span><span class="sxs-lookup"><span data-stu-id="03215-121">Feature\_Parent</span></span> |
|---------------|------------|-----------------|
| <span data-ttu-id="03215-122">Спорт</span><span class="sxs-lookup"><span data-stu-id="03215-122">Sport</span></span>         | <span data-ttu-id="03215-123">4</span><span class="sxs-lookup"><span data-stu-id="03215-123">4</span></span>          | <span data-ttu-id="03215-124">Спорт</span><span class="sxs-lookup"><span data-stu-id="03215-124">Sport</span></span>           |
| <span data-ttu-id="03215-125">Swimming</span><span class="sxs-lookup"><span data-stu-id="03215-125">Swimming</span></span>      | <span data-ttu-id="03215-126">1</span><span class="sxs-lookup"><span data-stu-id="03215-126">1</span></span>          | <span data-ttu-id="03215-127">Спорт</span><span class="sxs-lookup"><span data-stu-id="03215-127">Sport</span></span>           |
| <span data-ttu-id="03215-128">Футбол</span><span class="sxs-lookup"><span data-stu-id="03215-128">Football</span></span>      | <span data-ttu-id="03215-129">4</span><span class="sxs-lookup"><span data-stu-id="03215-129">4</span></span>          | <span data-ttu-id="03215-130">Спорт</span><span class="sxs-lookup"><span data-stu-id="03215-130">Sport</span></span>           |
| <span data-ttu-id="03215-131">Freestyle</span><span class="sxs-lookup"><span data-stu-id="03215-131">Freestyle</span></span>     | <span data-ttu-id="03215-132">1</span><span class="sxs-lookup"><span data-stu-id="03215-132">1</span></span>          | <span data-ttu-id="03215-133">Swimming</span><span class="sxs-lookup"><span data-stu-id="03215-133">Swimming</span></span>        |
| <span data-ttu-id="03215-134">таучфутбалл</span><span class="sxs-lookup"><span data-stu-id="03215-134">TouchFootball</span></span> | <span data-ttu-id="03215-135">4</span><span class="sxs-lookup"><span data-stu-id="03215-135">4</span></span>          | <span data-ttu-id="03215-136">Футбол</span><span class="sxs-lookup"><span data-stu-id="03215-136">Football</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="03215-137">См. также</span><span class="sxs-lookup"><span data-stu-id="03215-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03215-138">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="03215-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



