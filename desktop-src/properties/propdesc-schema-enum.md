---
description: Используется для присвоения перечислимого текста дискретным значениям.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663401"
---
# <a name="enum"></a><span data-ttu-id="3f2a1-103">enum</span><span class="sxs-lookup"><span data-stu-id="3f2a1-103">enum</span></span>

<span data-ttu-id="3f2a1-104">Используется для присвоения перечислимого текста дискретным значениям.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-104">Used to assign enumerated text to discrete values.</span></span> <span data-ttu-id="3f2a1-105">В [енумератедлист](./propdesc-schema-enumeratedlist.md)может существовать любое количество этих элементов.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-105">Any number of these elements may exist under an [enumeratedList](./propdesc-schema-enumeratedlist.md).</span></span> <span data-ttu-id="3f2a1-106">Программным образом они представляются в виде объектов Ипропертенумтипе, чей метод [**ипропертенумтипе:: жетенумтипе**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) возвращает Pet \_ дискретевалуе.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-106">Programmatically, these are represented as IPropertyEnumType objects, whose [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) method returns PET\_DISCRETEVALUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f2a1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f2a1-107">Syntax</span></span>


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="3f2a1-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3f2a1-108">Element Information</span></span>



| <span data-ttu-id="3f2a1-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="3f2a1-109">Parent Element</span></span>                                         | <span data-ttu-id="3f2a1-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3f2a1-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="3f2a1-111">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="3f2a1-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="3f2a1-112">нет</span><span class="sxs-lookup"><span data-stu-id="3f2a1-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="3f2a1-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3f2a1-113">Attributes</span></span>



| <span data-ttu-id="3f2a1-114">Атрибут</span><span class="sxs-lookup"><span data-stu-id="3f2a1-114">Attribute</span></span> | <span data-ttu-id="3f2a1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3f2a1-115">Description</span></span>                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2a1-116">value</span><span class="sxs-lookup"><span data-stu-id="3f2a1-116">value</span></span>     | <span data-ttu-id="3f2a1-117">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-117">Public.</span></span> <span data-ttu-id="3f2a1-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-118">Required.</span></span> <span data-ttu-id="3f2a1-119">Дискретное значение (строка или число), которому присваивается перечислимый текст.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-119">The discrete value (string or number) to be assigned enumerated text to.</span></span>                                                                                                                           |
| <span data-ttu-id="3f2a1-120">text</span><span class="sxs-lookup"><span data-stu-id="3f2a1-120">text</span></span>      | <span data-ttu-id="3f2a1-121">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-121">Public.</span></span> <span data-ttu-id="3f2a1-122">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-122">Required.</span></span> <span data-ttu-id="3f2a1-123">Текст, используемый для вывода перечислимого значения.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-123">The text used to display the enumerated value.</span></span> <span data-ttu-id="3f2a1-124">Синтаксис допускает прямую отображаемую строку или ссылку на непрямо отображаемую строку; Используйте строку с косвенным отображением, чтобы ее можно было локализовать.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-124">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span> |
| <span data-ttu-id="3f2a1-125">назначенные клавиши</span><span class="sxs-lookup"><span data-stu-id="3f2a1-125">mnemonics</span></span> | <span data-ttu-id="3f2a1-126">**Windows 7 и более поздние версии.**</span><span class="sxs-lookup"><span data-stu-id="3f2a1-126">**Windows 7 and later.**</span></span> <span data-ttu-id="3f2a1-127">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-127">Public.</span></span> <span data-ttu-id="3f2a1-128">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-128">Optional.</span></span> <span data-ttu-id="3f2a1-129">Список назначенных значений, которые можно использовать для ссылки на свойство в поисковых запросах.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-129">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="3f2a1-130">Список отделяется \| символом "".</span><span class="sxs-lookup"><span data-stu-id="3f2a1-130">The list is delimited with the '\|' character.</span></span>                                     |



 

 

 
