---
description: Указывает список предпочтительных поставщиков сети во время перемещения.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Датароамингпартнерс (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656539"
---
# <a name="dataroamingpartners-mbnprofile-element"></a><span data-ttu-id="34295-103">Датароамингпартнерс (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="34295-103">DataRoamingPartners (MBNProfile) Element</span></span>

<span data-ttu-id="34295-104">Элемент **датароамингпартнерс (мбнпрофиле)** указывает список предпочтительных поставщиков сети во время перемещения.</span><span class="sxs-lookup"><span data-stu-id="34295-104">The **DataRoamingPartners (MBNProfile)** element specifies the list of preferred network providers at the time of roaming.</span></span>

<span data-ttu-id="34295-105">Служба мобильной широкополосной связи использует этот элемент, чтобы выбрать предпочитаемую сеть в роуминге.</span><span class="sxs-lookup"><span data-stu-id="34295-105">The Mobile Broadband service uses this element to select the preferred network provide while roaming.</span></span>

<span data-ttu-id="34295-106">Элемент имеет следующий дочерний элемент, который должен быть определен по крайней мере один раз, но может быть определен несколько раз.</span><span class="sxs-lookup"><span data-stu-id="34295-106">The element has the following child element which must be defined at least once but can be defined multiple times.</span></span>

-   [<span data-ttu-id="34295-107">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="34295-107">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md)

<span data-ttu-id="34295-108">Этот элемент может иметь максимум одно вхождение.</span><span class="sxs-lookup"><span data-stu-id="34295-108">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="34295-109">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="34295-109">This element is optional.</span></span>

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="34295-110">Элемент **датароамингпартнерс** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="34295-110">The **DataRoamingPartners** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="34295-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="34295-111">Child elements</span></span>



| <span data-ttu-id="34295-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="34295-112">Element</span></span>                                                         | <span data-ttu-id="34295-113">Тип</span><span class="sxs-lookup"><span data-stu-id="34295-113">Type</span></span>                                                    | <span data-ttu-id="34295-114">Описание</span><span class="sxs-lookup"><span data-stu-id="34295-114">Description</span></span>                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="34295-115">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="34295-115">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md) | [<span data-ttu-id="34295-116">**providerType**</span><span class="sxs-lookup"><span data-stu-id="34295-116">**providerType**</span></span>](schema-providertype-complextype.md) | <span data-ttu-id="34295-117">Имя и идентификатор поставщика сотовой сети.</span><span class="sxs-lookup"><span data-stu-id="34295-117">Name and provider ID of a cellular network.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="34295-118">Требования</span><span class="sxs-lookup"><span data-stu-id="34295-118">Requirements</span></span>



| <span data-ttu-id="34295-119">Требование</span><span class="sxs-lookup"><span data-stu-id="34295-119">Requirement</span></span> | <span data-ttu-id="34295-120">Значение</span><span class="sxs-lookup"><span data-stu-id="34295-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="34295-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34295-121">Minimum supported client</span></span><br/> | <span data-ttu-id="34295-122">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="34295-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="34295-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34295-123">Minimum supported server</span></span><br/> | <span data-ttu-id="34295-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="34295-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="34295-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34295-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="34295-126">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="34295-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="34295-127">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="34295-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="34295-128">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="34295-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="34295-129">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="34295-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




