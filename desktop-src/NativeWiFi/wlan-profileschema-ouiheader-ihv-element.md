---
description: Идентифицирует независимый поставщик оборудования.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Ауихеадер (IHV), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673242"
---
# <a name="ouiheader-ihv-element"></a><span data-ttu-id="2d4e8-103">Ауихеадер (IHV), элемент</span><span class="sxs-lookup"><span data-stu-id="2d4e8-103">OUIHeader (IHV) Element</span></span>

<span data-ttu-id="2d4e8-104">Элемент Ауихеадер (IHV) идентифицирует независимый поставщик оборудования.</span><span class="sxs-lookup"><span data-stu-id="2d4e8-104">The OUIHeader (IHV) element identifies the IHV.</span></span>

<span data-ttu-id="2d4e8-105">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2d4e8-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="type">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="1"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2d4e8-106">Элемент определяется элементом [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2d4e8-106">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2d4e8-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2d4e8-107">Child elements</span></span>



| <span data-ttu-id="2d4e8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="2d4e8-108">Element</span></span>                                                   | <span data-ttu-id="2d4e8-109">Тип</span><span class="sxs-lookup"><span data-stu-id="2d4e8-109">Type</span></span> | <span data-ttu-id="2d4e8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2d4e8-110">Description</span></span>                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d4e8-111">**КОДОМ**</span><span class="sxs-lookup"><span data-stu-id="2d4e8-111">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)   |      | <span data-ttu-id="2d4e8-112">Содержит 3-байтовый hexBinary, определяющий IHV.</span><span class="sxs-lookup"><span data-stu-id="2d4e8-112">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                            |
| [<span data-ttu-id="2d4e8-113">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2d4e8-113">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md) |      | <span data-ttu-id="2d4e8-114">Содержит 1-байтовый hexBinary, используемый для различения сетевых карт одним и тем же IHV.</span><span class="sxs-lookup"><span data-stu-id="2d4e8-114">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2d4e8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2d4e8-115">Requirements</span></span>



| <span data-ttu-id="2d4e8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2d4e8-116">Requirement</span></span> | <span data-ttu-id="2d4e8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2d4e8-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d4e8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d4e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d4e8-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d4e8-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d4e8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d4e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d4e8-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d4e8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d4e8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d4e8-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d4e8-123">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="2d4e8-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2d4e8-124">**АППАРАТ**</span><span class="sxs-lookup"><span data-stu-id="2d4e8-124">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="2d4e8-125">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="2d4e8-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2d4e8-126">**IHV (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="2d4e8-126">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




