---
description: Содержит 1-байтовый hexBinary, используемый для различения сетевых карт, созданных одним и тем же IHV.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: Элемент Type (Ауихеадер)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910647"
---
# <a name="type-ouiheader-element"></a><span data-ttu-id="d978e-103">Элемент Type (Ауихеадер)</span><span class="sxs-lookup"><span data-stu-id="d978e-103">type (OUIHeader) Element</span></span>

<span data-ttu-id="d978e-104">Элемент Type (Ауихеадер) содержит 1-байтный hexBinary, который используется для различения сетевых карт, созданных одним и тем же IHV.</span><span class="sxs-lookup"><span data-stu-id="d978e-104">The type (OUIHeader) element contains a 1-byte hexBinary that is used to differentiate between NICs made by the same IHV.</span></span>

<span data-ttu-id="d978e-105">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d978e-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="d978e-106">Элемент определяется элементом [**ауихеадер**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d978e-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d978e-107">Требования</span><span class="sxs-lookup"><span data-stu-id="d978e-107">Requirements</span></span>



| <span data-ttu-id="d978e-108">Требование</span><span class="sxs-lookup"><span data-stu-id="d978e-108">Requirement</span></span> | <span data-ttu-id="d978e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="d978e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d978e-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d978e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d978e-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d978e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d978e-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d978e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d978e-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d978e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d978e-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d978e-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="d978e-115">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="d978e-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d978e-116">**ауихеадер**</span><span class="sxs-lookup"><span data-stu-id="d978e-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="d978e-117">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="d978e-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d978e-118">**Ауихеадер (IHV)**</span><span class="sxs-lookup"><span data-stu-id="d978e-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




