---
description: Указывает, будет ли общий ключ представлять собой сетевой ключ или парольную фразу.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: keyType (sharedKey), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673867"
---
# <a name="keytype-sharedkey-element"></a><span data-ttu-id="075d6-103">keyType (sharedKey), элемент</span><span class="sxs-lookup"><span data-stu-id="075d6-103">keyType (sharedKey) Element</span></span>

<span data-ttu-id="075d6-104">Элемент keyType (sharedKey) указывает, будет ли общий ключ представлять собой сетевой ключ или парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="075d6-104">The keyType (sharedKey) element indicates whether the shared key will be a network key or a pass phrase.</span></span>

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="075d6-105">Элемент определяется элементом [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="075d6-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="075d6-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="075d6-106">Remarks</span></span>

<span data-ttu-id="075d6-107">Если элемент [**ENCRYPTION**](wlan-profileschema-encryption-authencryption-element.md) имеет значение WEP, для параметра **KeyType** должен быть задан параметр **нетворккэй**.</span><span class="sxs-lookup"><span data-stu-id="075d6-107">When the [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of WEP, **keyType** must be set to **networkKey**.</span></span>

## <a name="examples"></a><span data-ttu-id="075d6-108">Примеры</span><span class="sxs-lookup"><span data-stu-id="075d6-108">Examples</span></span>

<span data-ttu-id="075d6-109">Для просмотра образцов профилей, использующих элемент **KeyType** , см. пример [профиля без широковещательной рассылки](non-broadcast-profile-sample.md), [пример профиля WPA-личное](wpa-personal-profile-sample.md)и [профиль WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="075d6-109">To view sample profiles that use the **keyType** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="075d6-110">Требования</span><span class="sxs-lookup"><span data-stu-id="075d6-110">Requirements</span></span>



| <span data-ttu-id="075d6-111">Требование</span><span class="sxs-lookup"><span data-stu-id="075d6-111">Requirement</span></span> | <span data-ttu-id="075d6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="075d6-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="075d6-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="075d6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="075d6-114">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="075d6-114">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="075d6-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="075d6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="075d6-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="075d6-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="075d6-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="075d6-117">Redistributable</span></span><br/>          | <span data-ttu-id="075d6-118">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="075d6-118">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="075d6-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="075d6-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="075d6-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="075d6-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="075d6-121">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="075d6-121">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="075d6-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="075d6-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="075d6-123">**sharedKey (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="075d6-123">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




