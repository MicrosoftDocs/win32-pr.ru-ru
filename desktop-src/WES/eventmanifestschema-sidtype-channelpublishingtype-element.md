---
title: Идентификатор типа безопасности (Чаннелпублишингтипе), элемент
description: Определяет, следует ли включать идентификатор безопасности (SID) участника с каждым событием, записанным в канал.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- Журнал событий элемента идентификатор типа безопасности
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691864"
---
# <a name="sidtype-channelpublishingtype-element"></a><span data-ttu-id="55eac-104">Идентификатор типа безопасности (Чаннелпублишингтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="55eac-104">sidType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="55eac-105">Определяет, следует ли включать идентификатор безопасности (SID) участника с каждым событием, записанным в канал.</span><span class="sxs-lookup"><span data-stu-id="55eac-105">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span>

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="55eac-106">Элемент **идентификатор типа безопасности** определяется сложным типом [**чаннелпублишингтипе**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="55eac-106">The **sidType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="55eac-107">Требования</span><span class="sxs-lookup"><span data-stu-id="55eac-107">Requirements</span></span>



| <span data-ttu-id="55eac-108">Требование</span><span class="sxs-lookup"><span data-stu-id="55eac-108">Requirement</span></span> | <span data-ttu-id="55eac-109">Значение</span><span class="sxs-lookup"><span data-stu-id="55eac-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55eac-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55eac-110">Minimum supported client</span></span><br/> | <span data-ttu-id="55eac-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55eac-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55eac-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55eac-112">Minimum supported server</span></span><br/> | <span data-ttu-id="55eac-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55eac-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55eac-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55eac-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="55eac-115">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="55eac-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="55eac-116">**Публикация (Чаннелтипе)**</span><span class="sxs-lookup"><span data-stu-id="55eac-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





