---
description: Изображение
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Элемент Image (схема описания свойства)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104992"
---
# <a name="image"></a><span data-ttu-id="aeffc-103">Изображение</span><span class="sxs-lookup"><span data-stu-id="aeffc-103">image</span></span>

<span data-ttu-id="aeffc-104">Для каждого родительского элемента должен быть только один элемент [Image]() .</span><span class="sxs-lookup"><span data-stu-id="aeffc-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeffc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aeffc-105">Syntax</span></span>


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="aeffc-106">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="aeffc-106">Element Information</span></span>



| <span data-ttu-id="aeffc-107">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="aeffc-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="aeffc-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="aeffc-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="aeffc-109">[enum](./propdesc-schema-enum.md), [енумранже](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="aeffc-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="aeffc-110">None</span><span class="sxs-lookup"><span data-stu-id="aeffc-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="aeffc-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="aeffc-111">Attributes</span></span>



| <span data-ttu-id="aeffc-112">Атрибут</span><span class="sxs-lookup"><span data-stu-id="aeffc-112">Attribute</span></span> | <span data-ttu-id="aeffc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="aeffc-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="aeffc-114">res</span><span class="sxs-lookup"><span data-stu-id="aeffc-114">res</span></span>       | <span data-ttu-id="aeffc-115">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="aeffc-115">Public.</span></span> <span data-ttu-id="aeffc-116">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="aeffc-116">Required.</span></span> |



 

 

 
