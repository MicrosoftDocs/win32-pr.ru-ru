---
description: Система свойств содержит свойство System. Kind, которое делит элементы на типы в соответствии с расширением имени файла, и какие конечные пользователи могут легко найти в.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Использование имен видов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344815"
---
# <a name="using-kind-names"></a><span data-ttu-id="1c7b9-103">Использование имен видов</span><span class="sxs-lookup"><span data-stu-id="1c7b9-103">Using Kind Names</span></span>

<span data-ttu-id="1c7b9-104">Система свойств содержит свойство `System.Kind` с именем, которое делит элементы на типы в соответствии с расширением имени файла, и какие пользователи могут легко опознать с помощью.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="1c7b9-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1c7b9-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1c7b9-106">Сведения о свойстве System. Kind</span><span class="sxs-lookup"><span data-stu-id="1c7b9-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="1c7b9-107">Иерархия и регистрация значения типа</span><span class="sxs-lookup"><span data-stu-id="1c7b9-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="1c7b9-108">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1c7b9-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="1c7b9-109">См. также</span><span class="sxs-lookup"><span data-stu-id="1c7b9-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="1c7b9-110">Сведения о свойстве System. Kind</span><span class="sxs-lookup"><span data-stu-id="1c7b9-110">About the System.Kind Property</span></span>

<span data-ttu-id="1c7b9-111">Тип появился в Windows Vista, чтобы выразить более удобное для пользователя понятие типа файла.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="1c7b9-112">`System.Kind`Свойство делит элементы на типы и предоставляет имя типа, с помощью которого пользователи могут выполнять поиск, например документы, музыку, изображения и т. д.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="1c7b9-113">Таким образом, имена типов известны как понятные пользователю.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="1c7b9-114">Так как `System.Kind` свойство имеет одно и то же значение для элементов одного типа файлов и связывает элементы, имеющие аналогичные характеристики с общим свойством, система и пользователь могут работать с группой в целом.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="1c7b9-115">Например, `System.Kind` свойство можно использовать для ограничения поиска по элементам определенного типа, отображения наиболее релевантных свойств элемента в представлении содержимого или группирования аналогичных элементов вместе.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="1c7b9-116">Поскольку Kind является строковым свойством с несколькими значениями, можно использовать `audio;video` `link;document` значение типа или.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="1c7b9-117">`System.Kind`Значения — это упорядоченный список строковых значений.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="1c7b9-118">В некоторых случаях в этом списке может быть только один элемент.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="1c7b9-119">В других случаях элемент может принадлежать более чем одному виду.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="1c7b9-120">Пример элемента, принадлежащего более чем одному виду, см. в примере раздела реестра в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="1c7b9-121">Строковые значения задаются из предопределенного набора известных значений.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="1c7b9-122">Значения сравниваются с использованием функций сравнения строк, не учитывающих регистр и не учитывающих язык и региональные параметры.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="1c7b9-123">Эти строки не локализуются.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-123">These strings are not localized.</span></span>

<span data-ttu-id="1c7b9-124">Некоторые имена типов уже связаны со свойствами и шаблонами макета.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="1c7b9-125">Например, элементы, связанные с `Kind.Picture` , и элементы, связанные с, `Kind.Document` отображают различные свойства, даже если они находятся в одном представлении, из-за свойств и шаблонов макета, которые уже связаны с этими двумя именами типов.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="1c7b9-126">Тип каждого элемента можно связать с одним из четырех уникальных шаблонов макета, определяющих количество свойств, отображаемых для каждого элемента и их макета.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="1c7b9-127">Дополнительные сведения см. в разделе [представление содержимого на основе типа файла или связи типа](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c7b9-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="1c7b9-128">Иерархия и регистрация значения типа</span><span class="sxs-lookup"><span data-stu-id="1c7b9-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="1c7b9-129">`Kind`Значение должно представлять одно из значений из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-129">A `Kind` value must represent one of the values in the following list.</span></span>

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

<span data-ttu-id="1c7b9-130">Обработчики свойств могут объявить свое `System.Kind` свойство статически через реестр, или они могут динамически предоставлять значение через свой код, как в случае со стандартным свойством.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="1c7b9-131">Чтобы статически определить `Kind` свойство, в раздел реестра **киндмап** добавляется запись с параметром **reg \_ SZ** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

<span data-ttu-id="1c7b9-132">Обратите внимание, что `Kind` может быть одиночным значением или несколькими значениями в строке, разделенной точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="1c7b9-133">При предоставлении нескольких значений сначала указывается наиболее конкретное `Kind` значение с наименьшим конкретным значением.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="1c7b9-134">В этом примере Contact имеет имя First, так как он является иерархически более конкретным, чем связь.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="1c7b9-135">Предполагается, что **элемент** value является неявным.</span><span class="sxs-lookup"><span data-stu-id="1c7b9-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c7b9-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1c7b9-136">Additional Resources</span></span>

-   <span data-ttu-id="1c7b9-137">Справочную документацию по свойствам см. в разделе [System. Kind](./props-system-kind.md) и [System. киндтекст](./props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="1c7b9-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="1c7b9-138">Дополнительные сведения о создании новых или использовании существующих типов файлов см. в разделе [типы файлов](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="1c7b9-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c7b9-139">См. также</span><span class="sxs-lookup"><span data-stu-id="1c7b9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c7b9-140">Основные сведения о обработчиках свойств</span><span class="sxs-lookup"><span data-stu-id="1c7b9-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="1c7b9-141">Использование списков свойств</span><span class="sxs-lookup"><span data-stu-id="1c7b9-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="1c7b9-142">Инициализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="1c7b9-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="1c7b9-143">Регистрация и распространение обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="1c7b9-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="1c7b9-144">Рекомендации и вопросы и ответы по обработчикам свойств</span><span class="sxs-lookup"><span data-stu-id="1c7b9-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
