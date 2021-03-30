---
description: Содержит сведения об авторе профиля.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Профилекреатионтипе (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145631"
---
# <a name="profilecreationtype-mbnprofile-element"></a><span data-ttu-id="ec6d9-103">Профилекреатионтипе (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="ec6d9-103">ProfileCreationType (MBNProfile) Element</span></span>

<span data-ttu-id="ec6d9-104">Элемент **профилекреатионтипе (мбнпрофиле)** содержит сведения об авторе профиля.</span><span class="sxs-lookup"><span data-stu-id="ec6d9-104">The **ProfileCreationType (MBNProfile)** element contains information about the creator of the profile.</span></span>

<span data-ttu-id="ec6d9-105">Этот элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ec6d9-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="ec6d9-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ec6d9-106">Value</span></span>                 | <span data-ttu-id="ec6d9-107">Значение</span><span class="sxs-lookup"><span data-stu-id="ec6d9-107">Meaning</span></span>                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6d9-108">"Усерпровисионед"</span><span class="sxs-lookup"><span data-stu-id="ec6d9-108">"UserProvisioned"</span></span>     | <span data-ttu-id="ec6d9-109">Этот профиль создается сведениями, предоставленными пользователем устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6d9-109">This profile is created by information provided by the user of device.</span></span>                                                     |
| <span data-ttu-id="ec6d9-110">"Админпровисионед"</span><span class="sxs-lookup"><span data-stu-id="ec6d9-110">"AdminProvisioned"</span></span>    | <span data-ttu-id="ec6d9-111">Этот профиль создается ИТ-администраторами и распространяется на пользователей.</span><span class="sxs-lookup"><span data-stu-id="ec6d9-111">This profile is created by IT administrators and distributed to users.</span></span>                                                     |
| <span data-ttu-id="ec6d9-112">"Операторпровисионед"</span><span class="sxs-lookup"><span data-stu-id="ec6d9-112">"OperatorProvisioned"</span></span> | <span data-ttu-id="ec6d9-113">Этот профиль создается сетевым оператором и распределяется между пользователями.</span><span class="sxs-lookup"><span data-stu-id="ec6d9-113">This profile is created by a network operator and distributed to users.</span></span>                                                    |
| <span data-ttu-id="ec6d9-114">"Девицепровисионед"</span><span class="sxs-lookup"><span data-stu-id="ec6d9-114">"DeviceProvisioned"</span></span>   | <span data-ttu-id="ec6d9-115">Этот профиль создается службой мобильной широкополосной связи с использованием сведений, хранящихся в подготовленном для устройства контексте.</span><span class="sxs-lookup"><span data-stu-id="ec6d9-115">This profile is created by the Mobile Broadband service by using the information stored in the device provisioned context.</span></span> |



 

<span data-ttu-id="ec6d9-116">Это необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ec6d9-116">This is an optional element.</span></span>

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ec6d9-117">Элемент **профилекреатионтипе** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ec6d9-117">The **ProfileCreationType** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec6d9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ec6d9-118">Requirements</span></span>



| <span data-ttu-id="ec6d9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ec6d9-119">Requirement</span></span> | <span data-ttu-id="ec6d9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ec6d9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ec6d9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec6d9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec6d9-122">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ec6d9-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ec6d9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec6d9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec6d9-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ec6d9-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ec6d9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec6d9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec6d9-126">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ec6d9-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ec6d9-127">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="ec6d9-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="ec6d9-128">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ec6d9-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ec6d9-129">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="ec6d9-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




