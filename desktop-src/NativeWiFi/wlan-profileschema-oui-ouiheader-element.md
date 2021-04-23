---
description: Содержит 3-байтовый hexBinary, определяющий IHV.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: Элемент OUI (Ауихеадер)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682601"
---
# <a name="oui-ouiheader-element"></a><span data-ttu-id="7cd70-103">Элемент OUI (Ауихеадер)</span><span class="sxs-lookup"><span data-stu-id="7cd70-103">OUI (OUIHeader) Element</span></span>

<span data-ttu-id="7cd70-104">Элемент OUI (Ауихеадер) содержит 3-байтовый hexBinary, определяющий IHV.</span><span class="sxs-lookup"><span data-stu-id="7cd70-104">The OUI (OUIHeader) element contains a 3 byte hexBinary that identifies the IHV.</span></span>

<span data-ttu-id="7cd70-105">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7cd70-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="7cd70-106">Элемент определяется элементом [**ауихеадер**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7cd70-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd70-107">Требования</span><span class="sxs-lookup"><span data-stu-id="7cd70-107">Requirements</span></span>



| <span data-ttu-id="7cd70-108">Требование</span><span class="sxs-lookup"><span data-stu-id="7cd70-108">Requirement</span></span> | <span data-ttu-id="7cd70-109">Значение</span><span class="sxs-lookup"><span data-stu-id="7cd70-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7cd70-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7cd70-110">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd70-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7cd70-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7cd70-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7cd70-112">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd70-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7cd70-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cd70-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cd70-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="7cd70-115">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="7cd70-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7cd70-116">**ауихеадер**</span><span class="sxs-lookup"><span data-stu-id="7cd70-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="7cd70-117">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="7cd70-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7cd70-118">**Ауихеадер (IHV)**</span><span class="sxs-lookup"><span data-stu-id="7cd70-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




