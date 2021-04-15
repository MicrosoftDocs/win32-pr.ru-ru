---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Элемент Image (схема описания свойства)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662768"
---
# <a name="image"></a><span data-ttu-id="02586-103">Изображение</span><span class="sxs-lookup"><span data-stu-id="02586-103">image</span></span>

<span data-ttu-id="02586-104">Для каждого родительского элемента должен быть только один элемент [Image]() .</span><span class="sxs-lookup"><span data-stu-id="02586-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="02586-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02586-105">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="02586-106">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="02586-106">Element Information</span></span>



| <span data-ttu-id="02586-107">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="02586-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="02586-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="02586-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="02586-109">[enum](./propdesc-schema-enum.md), [енумранже](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="02586-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="02586-110">Нет</span><span class="sxs-lookup"><span data-stu-id="02586-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="02586-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="02586-111">Attributes</span></span>



| <span data-ttu-id="02586-112">Атрибут</span><span class="sxs-lookup"><span data-stu-id="02586-112">Attribute</span></span> | <span data-ttu-id="02586-113">Описание</span><span class="sxs-lookup"><span data-stu-id="02586-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="02586-114">res</span><span class="sxs-lookup"><span data-stu-id="02586-114">res</span></span>       | <span data-ttu-id="02586-115">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="02586-115">Public.</span></span> <span data-ttu-id="02586-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="02586-116">Required.</span></span> |



 

 

 
