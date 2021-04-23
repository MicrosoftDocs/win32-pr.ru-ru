---
description: Указывает режим работы сети.
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: Элемент connectionType (Вланпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1e7b456260c656ebb3d64b6a3732fe97ca3ca488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898117"
---
# <a name="connectiontype-wlanprofile-element"></a><span data-ttu-id="064a6-103">Элемент connectionType (Вланпрофиле)</span><span class="sxs-lookup"><span data-stu-id="064a6-103">connectionType (WLANProfile) Element</span></span>

<span data-ttu-id="064a6-104">Элемент connectionType (Вланпрофиле) указывает режим работы сети.</span><span class="sxs-lookup"><span data-stu-id="064a6-104">The connectionType (WLANProfile) element indicates the operating mode of the network.</span></span>

<span data-ttu-id="064a6-105">Значение **ESS** указывает на сеть инфраструктуры, а **ибсс** — на нерегламентированную сеть.</span><span class="sxs-lookup"><span data-stu-id="064a6-105">A value of **ESS** indicates an infrastructure network, while **IBSS** indicates an ad-hoc network.</span></span>

``` syntax
<xs:element name="connectionType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="IBSS"
             />
            <xs:enumeration
                value="ESS"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="064a6-106">Элемент **connectionType** определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="064a6-106">The **connectionType** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="064a6-107">Примеры</span><span class="sxs-lookup"><span data-stu-id="064a6-107">Examples</span></span>

<span data-ttu-id="064a6-108">Чтобы просмотреть образцы профилей, в которых используется элемент **connectionType** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="064a6-108">To view sample profiles that use the **connectionType** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="064a6-109">Требования</span><span class="sxs-lookup"><span data-stu-id="064a6-109">Requirements</span></span>



| <span data-ttu-id="064a6-110">Требование</span><span class="sxs-lookup"><span data-stu-id="064a6-110">Requirement</span></span> | <span data-ttu-id="064a6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="064a6-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="064a6-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="064a6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="064a6-113">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="064a6-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="064a6-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="064a6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="064a6-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="064a6-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="064a6-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="064a6-116">Redistributable</span></span><br/>          | <span data-ttu-id="064a6-117">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="064a6-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="064a6-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="064a6-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="064a6-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="064a6-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="064a6-120">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="064a6-120">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="064a6-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="064a6-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="064a6-122">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="064a6-122">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




