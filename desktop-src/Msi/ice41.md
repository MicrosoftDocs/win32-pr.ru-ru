---
description: ICE41 проверяет, ссылаются ли записи в таблицах классов и расширений на записи в таблице Component, реализующие объект класса или расширение компонента.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650927"
---
# <a name="ice41"></a><span data-ttu-id="53ad1-103">ICE41</span><span class="sxs-lookup"><span data-stu-id="53ad1-103">ICE41</span></span>

<span data-ttu-id="53ad1-104">ICE41 проверяет, ссылаются ли записи в таблицах [классов](class-table.md) и [расширений](extension-table.md) на записи в [таблице Component](component-table.md) , реализующие объект класса или расширение компонента.</span><span class="sxs-lookup"><span data-stu-id="53ad1-104">ICE41 validates that the entries in the [Class](class-table.md) and [Extension](extension-table.md) tables refer to entries in the [Component table](component-table.md) that implement the class object or extension of the component.</span></span>

## <a name="result"></a><span data-ttu-id="53ad1-105">Результат</span><span class="sxs-lookup"><span data-stu-id="53ad1-105">Result</span></span>

<span data-ttu-id="53ad1-106">ICE41 отправляет сообщение об ошибке, если имеется функция, которая не содержит компонент, реализующий объект класса или расширение.</span><span class="sxs-lookup"><span data-stu-id="53ad1-106">ICE41 posts an error if there is a feature that does not contain the component implementing the class object or extension.</span></span>

## <a name="example"></a><span data-ttu-id="53ad1-107">Пример</span><span class="sxs-lookup"><span data-stu-id="53ad1-107">Example</span></span>

<span data-ttu-id="53ad1-108">ICE41 сообщает о следующих ошибках в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="53ad1-108">ICE41 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="53ad1-109">ICE41, ошибка</span><span class="sxs-lookup"><span data-stu-id="53ad1-109">ICE41 error</span></span>                                                                                                                                                                                    | <span data-ttu-id="53ad1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="53ad1-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53ad1-111">Класс {00000000-0000-0000-0000-0000000000000} ссылается на компонент Feature2 и компонент Component1, но этот компонент не связан с этой функцией в таблице феатурекомпонентс.</span><span class="sxs-lookup"><span data-stu-id="53ad1-111">Class {00000000-0000-0000-0000-0000000000000} references feature Feature2 and component Component1, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span> | <span data-ttu-id="53ad1-112">Существует функция, которая не содержит компонент, реализующий объект класса.</span><span class="sxs-lookup"><span data-stu-id="53ad1-112">There is a feature that does not contain the component implementing the class object.</span></span> <span data-ttu-id="53ad1-113">Это означает, что установщик не устанавливает компонент с компонентом, и эта реклама может не работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="53ad1-113">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="53ad1-114">Чтобы устранить эту ошибку, измените запись в столбце "компонент \_ " в записи [таблицы класса](class-table.md) , чтобы она ссылалась на компонент установки компонента, указанного в \_ столбце Component, или изменить функцию и компонент, связанные с [таблицей феатурекомпонентс](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="53ad1-114">To fix this error, change the entry in the Feature\_ column of the [Class table](class-table.md) entry to reference a feature that installs component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/>          |
| <span data-ttu-id="53ad1-115">Extension. ИП ссылается на компоненты Feature1 и Component Component2, но этот компонент не связан с этой функцией в таблице Феатурекомпонентс.</span><span class="sxs-lookup"><span data-stu-id="53ad1-115">Extension .yip references feature Feature1 and component Component2, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span>                                | <span data-ttu-id="53ad1-116">Существует функция, которая не содержит компонент, реализующий расширение.</span><span class="sxs-lookup"><span data-stu-id="53ad1-116">There is a feature that does not contain the component implementing the extension.</span></span> <span data-ttu-id="53ad1-117">Это означает, что установщик не устанавливает компонент с компонентом, и эта реклама может не работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="53ad1-117">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="53ad1-118">Чтобы устранить эту ошибку, измените запись в столбце "компонент" в \_ записи [таблицы расширений](extension-table.md) , чтобы она ссылалась на компонент установки компонента, указанного в столбце Component, \_ или изменить функцию и компонент, связанные с [таблицей феатурекомпонентс](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="53ad1-118">To fix this error, change the entry in the Feature\_ column of the [Extension table](extension-table.md) entry to reference a feature that installs the component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/> |



 

<span data-ttu-id="53ad1-119">[Таблица феатурекомпонентс](featurecomponents-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="53ad1-119">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="53ad1-120">Функция\_</span><span class="sxs-lookup"><span data-stu-id="53ad1-120">Feature\_</span></span> |
|-----------|
| <span data-ttu-id="53ad1-121">Feature1</span><span class="sxs-lookup"><span data-stu-id="53ad1-121">Feature1</span></span>  |
| <span data-ttu-id="53ad1-122">Feature2</span><span class="sxs-lookup"><span data-stu-id="53ad1-122">Feature2</span></span>  |



 

<span data-ttu-id="53ad1-123">[Таблица классов](class-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="53ad1-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="53ad1-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="53ad1-124">CLSID</span></span>                                  | <span data-ttu-id="53ad1-125">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="53ad1-125">Component\_</span></span> | <span data-ttu-id="53ad1-126">Функция\_</span><span class="sxs-lookup"><span data-stu-id="53ad1-126">Feature\_</span></span> |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | <span data-ttu-id="53ad1-127">Component1</span><span class="sxs-lookup"><span data-stu-id="53ad1-127">Component1</span></span>  | <span data-ttu-id="53ad1-128">Feature2</span><span class="sxs-lookup"><span data-stu-id="53ad1-128">Feature2</span></span>  |



 

<span data-ttu-id="53ad1-129">[Таблица классов](class-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="53ad1-129">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="53ad1-130">Расширение</span><span class="sxs-lookup"><span data-stu-id="53ad1-130">Extension</span></span> | <span data-ttu-id="53ad1-131">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="53ad1-131">Component\_</span></span> | <span data-ttu-id="53ad1-132">Функция\_</span><span class="sxs-lookup"><span data-stu-id="53ad1-132">Feature\_</span></span> |
|-----------|-------------|-----------|
| <span data-ttu-id="53ad1-133">. ИП</span><span class="sxs-lookup"><span data-stu-id="53ad1-133">.yip</span></span>      | <span data-ttu-id="53ad1-134">Component2</span><span class="sxs-lookup"><span data-stu-id="53ad1-134">Component2</span></span>  | <span data-ttu-id="53ad1-135">Feature1</span><span class="sxs-lookup"><span data-stu-id="53ad1-135">Feature1</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="53ad1-136">См. также</span><span class="sxs-lookup"><span data-stu-id="53ad1-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53ad1-137">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="53ad1-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




