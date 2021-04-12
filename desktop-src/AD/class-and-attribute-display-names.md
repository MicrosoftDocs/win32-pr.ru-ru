---
title: Отображаемые имена классов и атрибутов
description: В этом разделе содержатся сведения и рекомендации по отображаемым именам классов и атрибутов.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- Спецификаторы экрана AD, отображаемые имена классов и атрибутов
- отображаемые имена классов AD
- отображаемые имена атрибутов AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487497"
---
# <a name="class-and-attribute-display-names"></a><span data-ttu-id="4aa3a-106">Отображаемые имена классов и атрибутов</span><span class="sxs-lookup"><span data-stu-id="4aa3a-106">Class and Attribute Display Names</span></span>

<span data-ttu-id="4aa3a-107">Описатель вывода для класса объекта содержит следующие атрибуты, которые можно использовать для указания локализованных отображаемых имен, используемых в пользовательском интерфейсе для объектов этого класса:</span><span class="sxs-lookup"><span data-stu-id="4aa3a-107">The display specifier for an object class contains the following attributes that can be used to specify the localized display names used in the UI for objects of that class:</span></span>

-   <span data-ttu-id="4aa3a-108">Атрибут **классдисплайнаме** представляет собой строку в Юникоде с одним значением, которая указывает отображаемое имя класса.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-108">The **classDisplayName** attribute is a single-value Unicode string that specifies the class display name.</span></span>
-   <span data-ttu-id="4aa3a-109">Атрибут **аттрибутедисплайнамес** является многозначным свойством, которое указывает имена, используемые в пользовательском интерфейсе для атрибутов класса Object.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-109">The **attributeDisplayNames** attribute is a multi-value property that specifies the names to use in the UI for attributes of the object class.</span></span>

<span data-ttu-id="4aa3a-110">Значения **аттрибутедисплайнамес** являются строками в Юникоде. Каждый элемент состоит из пары имен с разделителями-запятыми:</span><span class="sxs-lookup"><span data-stu-id="4aa3a-110">The **attributeDisplayNames** values are Unicode strings; each element consists of a comma-delimited name pair:</span></span>


```C++
<attribute name>,<display text>
```



<span data-ttu-id="4aa3a-111">В этом примере « &lt; имя атрибута» &gt; является атрибутом **lDAPDisplayName** атрибута, а « &lt; отображаемый текст &gt; » — текстом, отображаемым в пользовательском интерфейсе как имя этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-111">In this example, "&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute and "&lt;display text&gt;" is the text to display as the name of that attribute in the user interface.</span></span>

## <a name="guidelines-for-class-and-attribute-display-names"></a><span data-ttu-id="4aa3a-112">Рекомендации по отображаемым именам классов и атрибутов</span><span class="sxs-lookup"><span data-stu-id="4aa3a-112">Guidelines for Class and Attribute Display Names</span></span>

<span data-ttu-id="4aa3a-113">Поскольку многие поставщики могут расширять классы с новыми атрибутами или создавать совершенно новые классы, важно, чтобы отображаемые имена класса и атрибута были однозначными и не приводили к конфликтам.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-113">Because many vendors may extend classes with new attributes or creating entirely new classes, it is important that the class and attribute display names are unambiguous and do not result in conflicts.</span></span>

<span data-ttu-id="4aa3a-114">Каждый поставщик должен добавить к отображаемому имени класса префикс уникального понятного идентификатора на основе имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-114">Each vendor should prefix the class display name with a unique friendly identifier based on the vendor name.</span></span> <span data-ttu-id="4aa3a-115">Например, если вымышленная компания Fabrikam Inc. создает новый класс, производный от класса «Contact», у них может быть уникальное отображаемое имя класса «Контактное лицо Fabrikam».</span><span class="sxs-lookup"><span data-stu-id="4aa3a-115">For example, if the fictitious company, Fabrikam Inc., creates a new class derived from the "contact" class, they can have a unique class display name "Fabrikam Contact."</span></span>

<span data-ttu-id="4aa3a-116">Если поставщик расширяет существующий класс новыми атрибутами, он должен снова идентифицировать отображаемое имя атрибута, чтобы не возникало конфликтов с другими отображаемыми именами атрибутов.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-116">If a vendor extends an existing class with new attributes, they should again uniquely identify the attribute display name so that no conflicts occur with other attribute display names.</span></span> <span data-ttu-id="4aa3a-117">И опять же, рекомендуется префиксное имя атрибута с уникальным понятным идентификатором, основанное на имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-117">Again, prefixing the attribute display name with unique friendly identifier based on the vendor name is good practice.</span></span> <span data-ttu-id="4aa3a-118">Например, если компания Fabrikam расширяет класс пользователя с помощью нового атрибута HR, они могут уникальным образом отобразить атрибут как «сведения о ПЕРСОНАЛе Fabrikam».</span><span class="sxs-lookup"><span data-stu-id="4aa3a-118">For example, if the Fabrikam company extends the user class with a new HR attribute, they could uniquely display the attribute as "Fabrikam HR Information."</span></span>

<span data-ttu-id="4aa3a-119">Кроме того, с точки зрения локализации каждый поставщик должен локализовать отображаемые имена классов и атрибутов в каждом языке, поддерживаемом Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-119">In addition, from a localization perspective, each vendor should localize the class and attribute display names into each language supported by Windows 2000.</span></span>

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a><span data-ttu-id="4aa3a-120">Добавление значения к атрибуту Аттрибутедисплайнамес</span><span class="sxs-lookup"><span data-stu-id="4aa3a-120">Adding a Value to the attributeDisplayNames Attribute</span></span>

<span data-ttu-id="4aa3a-121">\*\*Добавление значения сопоставления имени в атрибут \*\*аттрибутедисплайнамес\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4aa3a-121">**To add a name mapping value to the **attributeDisplayNames** attribute**</span></span>

1.  <span data-ttu-id="4aa3a-122">Определить, существует ли значение сопоставления имен для атрибута.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-122">Determine if the name mapping value for the attribute exists.</span></span> <span data-ttu-id="4aa3a-123">Если требуется заменить значение сопоставления имен, сначала удалите существующее значение с помощью метода [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) , где параметр *лнконтролкоде* установлен в значение **\_ свойства \_ ADS** , а параметр *впроп* — в удаляемое.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-123">If a name mapping value is to be replaced, first deleted the existing value, using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method, with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="4aa3a-124">Не используйте свойство **ADS \_ \_ Очистка** или **\_ \_ Обновление свойства ADS** для *лнконтролкоде*.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-124">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="4aa3a-125">Создайте строку, представляющую отображаемое имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-125">Create the string that represents the attribute display name.</span></span> <span data-ttu-id="4aa3a-126">Пример см. в приведенном выше формате.</span><span class="sxs-lookup"><span data-stu-id="4aa3a-126">For an example, see the format above.</span></span>
3.  <span data-ttu-id="4aa3a-127">Чтобы добавить новое значение, используйте метод [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) с параметром *лнконтролкоде* , для которого задано **\_ свойство ADS \_ append** .</span><span class="sxs-lookup"><span data-stu-id="4aa3a-127">Use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND** to add the new value.</span></span>
4.  <span data-ttu-id="4aa3a-128">Чтобы зафиксировать изменения в каталоге, вызовите функцию [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="4aa3a-128">Call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>

<span data-ttu-id="4aa3a-129">Дополнительные сведения о присвоении имен новым классам и атрибутам см. в разделе [именование атрибутов и классов](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="4aa3a-129">For more information about naming new classes and attributes, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>

 

 