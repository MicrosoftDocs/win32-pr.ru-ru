---
description: Указывает стандарт беспроводной локальной сети 802,11, используемый в беспроводной локальной сети.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Элемент Фитипе (Connectivity)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682600"
---
# <a name="phytype-connectivity-element"></a><span data-ttu-id="dc988-103">Элемент Фитипе (Connectivity)</span><span class="sxs-lookup"><span data-stu-id="dc988-103">phyType (connectivity) Element</span></span>

<span data-ttu-id="dc988-104">Элемент Фитипе (подключение) указывает стандарт беспроводной локальной сети 802,11, используемый в беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="dc988-104">The phyType (connectivity) element specifies the 802.11 wireless LAN standard used on a wireless LAN.</span></span>

<span data-ttu-id="dc988-105">Можно указать несколько **фитипе** s.</span><span class="sxs-lookup"><span data-stu-id="dc988-105">You can specify multiple **phyType** s.</span></span> <span data-ttu-id="dc988-106">Если **фитипе** не указан, профиль можно использовать для подключения к любому **фитипе**.</span><span class="sxs-lookup"><span data-stu-id="dc988-106">If no **phyType** is specified, the profile can be used to connect to any **phyType**.</span></span> <span data-ttu-id="dc988-107">Значение n поддерживается только в Windows Vista с пакетом обновления 1 (SP1) и более поздними версиями операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dc988-107">The value "n" is only supported on Windows Vista with Service Pack 1 (SP1) and later versions of the operating system.</span></span>

<span data-ttu-id="dc988-108">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc988-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="dc988-109">Элемент определяется элементом [**подключения**](wlan-profileschema-connectivity-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dc988-109">The element is defined by the [**connectivity**](wlan-profileschema-connectivity-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc988-110">Требования</span><span class="sxs-lookup"><span data-stu-id="dc988-110">Requirements</span></span>



| <span data-ttu-id="dc988-111">Требование</span><span class="sxs-lookup"><span data-stu-id="dc988-111">Requirement</span></span> | <span data-ttu-id="dc988-112">Значение</span><span class="sxs-lookup"><span data-stu-id="dc988-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc988-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc988-113">Minimum supported client</span></span><br/> | <span data-ttu-id="dc988-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc988-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc988-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc988-115">Minimum supported server</span></span><br/> | <span data-ttu-id="dc988-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc988-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc988-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc988-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc988-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="dc988-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="dc988-119">**установлен**</span><span class="sxs-lookup"><span data-stu-id="dc988-119">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

<span data-ttu-id="dc988-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="dc988-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="dc988-121">**подключение (MSM)**</span><span class="sxs-lookup"><span data-stu-id="dc988-121">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




