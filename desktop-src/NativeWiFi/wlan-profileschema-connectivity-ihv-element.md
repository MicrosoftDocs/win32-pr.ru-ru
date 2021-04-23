---
description: Содержит параметры подключения, связанные с IHV. В настоящее время он не реализован.
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: Элемент подключения (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 257addbcbd721e5930405e3954dcb348f367af93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811464"
---
# <a name="connectivity-ihv-element"></a><span data-ttu-id="0c96c-104">Элемент подключения (IHV)</span><span class="sxs-lookup"><span data-stu-id="0c96c-104">connectivity (IHV) Element</span></span>

<span data-ttu-id="0c96c-105">Элемент подключения (IHV) содержит параметры подключения, связанные с IHV.</span><span class="sxs-lookup"><span data-stu-id="0c96c-105">The connectivity (IHV) element contains IHV-related connectivity settings.</span></span> <span data-ttu-id="0c96c-106">В настоящее время он не реализован.</span><span class="sxs-lookup"><span data-stu-id="0c96c-106">It is not currently implemented.</span></span>

<span data-ttu-id="0c96c-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0c96c-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="0c96c-108">Элемент определяется элементом [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0c96c-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c96c-109">Требования</span><span class="sxs-lookup"><span data-stu-id="0c96c-109">Requirements</span></span>



| <span data-ttu-id="0c96c-110">Требование</span><span class="sxs-lookup"><span data-stu-id="0c96c-110">Requirement</span></span> | <span data-ttu-id="0c96c-111">Значение</span><span class="sxs-lookup"><span data-stu-id="0c96c-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c96c-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c96c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0c96c-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c96c-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c96c-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c96c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0c96c-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c96c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c96c-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c96c-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c96c-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="0c96c-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0c96c-118">**АППАРАТ**</span><span class="sxs-lookup"><span data-stu-id="0c96c-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="0c96c-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="0c96c-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0c96c-120">**IHV (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0c96c-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




