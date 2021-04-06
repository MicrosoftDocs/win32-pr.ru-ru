---
description: Присваивает текст перечисления диапазону значений. Каждый элемент Енумранже задает минимальное значение и расширяется до следующего минимального значения элемента или до тех пор, пока больше не будет элементов Енумранже.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: енумранже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991546"
---
# <a name="enumrange"></a><span data-ttu-id="a86c1-104">енумранже</span><span class="sxs-lookup"><span data-stu-id="a86c1-104">enumRange</span></span>

<span data-ttu-id="a86c1-105">Присваивает текст перечисления диапазону значений.</span><span class="sxs-lookup"><span data-stu-id="a86c1-105">Assigns enumeration text to a range of values.</span></span> <span data-ttu-id="a86c1-106">Каждый элемент [енумранже]() задает минимальное значение и расширяется до следующего минимального значения элемента или до тех пор, пока больше не будет элементов енумранже.</span><span class="sxs-lookup"><span data-stu-id="a86c1-106">Each [enumRange]() element specifies a minimum value, and extends until the next element minimum value, or until there are no more enumRange elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a86c1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a86c1-107">Syntax</span></span>

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="a86c1-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a86c1-108">Element Information</span></span>



| <span data-ttu-id="a86c1-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a86c1-109">Parent Element</span></span>                                         | <span data-ttu-id="a86c1-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a86c1-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="a86c1-111">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="a86c1-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="a86c1-112">нет</span><span class="sxs-lookup"><span data-stu-id="a86c1-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="a86c1-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a86c1-113">Attributes</span></span>



| <span data-ttu-id="a86c1-114">Атрибут</span><span class="sxs-lookup"><span data-stu-id="a86c1-114">Attribute</span></span> | <span data-ttu-id="a86c1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a86c1-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a86c1-116">minValue</span><span class="sxs-lookup"><span data-stu-id="a86c1-116">minValue</span></span>  | <span data-ttu-id="a86c1-117">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a86c1-117">Public.</span></span> <span data-ttu-id="a86c1-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a86c1-118">Required.</span></span> <span data-ttu-id="a86c1-119">Минимальное значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="a86c1-119">The minimum value in the range.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a86c1-120">setValue</span><span class="sxs-lookup"><span data-stu-id="a86c1-120">setValue</span></span>  | <span data-ttu-id="a86c1-121">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a86c1-121">Public.</span></span> <span data-ttu-id="a86c1-122">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a86c1-122">Optional.</span></span> <span data-ttu-id="a86c1-123">Когда пользователь выбирает это перечисление из элемента управления свойства ListBox, это дискретное значение присваивается как значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a86c1-123">When a user selects this enumeration from a listbox property control, this discrete value is assigned as the property value.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a86c1-124">text</span><span class="sxs-lookup"><span data-stu-id="a86c1-124">text</span></span>      | <span data-ttu-id="a86c1-125">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a86c1-125">Public.</span></span> <span data-ttu-id="a86c1-126">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a86c1-126">Optional.</span></span> <span data-ttu-id="a86c1-127">Текст, используемый для вывода перечислимого значения.</span><span class="sxs-lookup"><span data-stu-id="a86c1-127">The text used to display the enumerated value.</span></span> <span data-ttu-id="a86c1-128">Синтаксис допускает прямую отображаемую строку или ссылку на непрямо отображаемую строку; Используйте строку с косвенным отображением, чтобы ее можно было локализовать.</span><span class="sxs-lookup"><span data-stu-id="a86c1-128">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a86c1-129">назначенные клавиши</span><span class="sxs-lookup"><span data-stu-id="a86c1-129">mnemonics</span></span> | <span data-ttu-id="a86c1-130">**Windows 7 и более поздние версии.**</span><span class="sxs-lookup"><span data-stu-id="a86c1-130">**Windows 7 and later.**</span></span> <span data-ttu-id="a86c1-131">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="a86c1-131">Public.</span></span> <span data-ttu-id="a86c1-132">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a86c1-132">Optional.</span></span> <span data-ttu-id="a86c1-133">Список назначенных значений, которые можно использовать для ссылки на свойство в поисковых запросах.</span><span class="sxs-lookup"><span data-stu-id="a86c1-133">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="a86c1-134">Список отделяется \| символом "".</span><span class="sxs-lookup"><span data-stu-id="a86c1-134">The list is delimited with the '\|' character.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a86c1-135">name</span><span class="sxs-lookup"><span data-stu-id="a86c1-135">name</span></span>      | <span data-ttu-id="a86c1-136">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a86c1-136">Required.</span></span> <span data-ttu-id="a86c1-137">Каноническое имя свойства, уникальное для системы; Например, System. рейтинг.</span><span class="sxs-lookup"><span data-stu-id="a86c1-137">The canonical property name, unique to the system; for example, System.Rating.</span></span> <span data-ttu-id="a86c1-138">Длина этого атрибута ограничена 64 символами.</span><span class="sxs-lookup"><span data-stu-id="a86c1-138">This attribute is limited to 64 characters.</span></span> <span data-ttu-id="a86c1-139">Имя чувствительно к регистру и должно использовать следующий синтаксис: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="a86c1-139">The name is case sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="a86c1-140">Следующие методы возвращают это значение: [**иексплореркомманд:: жетканоникалнаме**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**Ипропертидескриптион:: жетканоникалнаме**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: Жетканоникалнаме**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)и [**IPropertyUI:: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a86c1-140">The following methods return this value: [**IExplorerCommand::GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2::GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2), and [**IPropertyUI::GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span></span> |



 

 

 
