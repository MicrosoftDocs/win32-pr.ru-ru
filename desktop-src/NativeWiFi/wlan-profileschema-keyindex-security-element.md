---
description: Указывает, какой индекс ключа следует использовать для шифрования беспроводного трафика. Используется, только если параметр keyType имеет значение &\# 0034; нетворккэй&\# 0034;.
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: Кэйиндекс (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156783"
---
# <a name="keyindex-security-element"></a><span data-ttu-id="36860-104">Кэйиндекс (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="36860-104">keyIndex (security) Element</span></span>

<span data-ttu-id="36860-105">Элемент Кэйиндекс (Security) указывает, какой индекс ключа следует использовать для шифрования беспроводного трафика.</span><span class="sxs-lookup"><span data-stu-id="36860-105">The keyIndex (security) element specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="36860-106">Используется, только если параметр [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) имеет значение "нетворккэй".</span><span class="sxs-lookup"><span data-stu-id="36860-106">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span>

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="36860-107">Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="36860-107">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="36860-108">Требования</span><span class="sxs-lookup"><span data-stu-id="36860-108">Requirements</span></span>



| <span data-ttu-id="36860-109">Требование</span><span class="sxs-lookup"><span data-stu-id="36860-109">Requirement</span></span> | <span data-ttu-id="36860-110">Значение</span><span class="sxs-lookup"><span data-stu-id="36860-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="36860-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36860-111">Minimum supported client</span></span><br/> | <span data-ttu-id="36860-112">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36860-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="36860-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36860-113">Minimum supported server</span></span><br/> | <span data-ttu-id="36860-114">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36860-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="36860-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="36860-115">Redistributable</span></span><br/>          | <span data-ttu-id="36860-116">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="36860-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="36860-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36860-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="36860-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="36860-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="36860-119">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="36860-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="36860-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="36860-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="36860-121">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="36860-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




