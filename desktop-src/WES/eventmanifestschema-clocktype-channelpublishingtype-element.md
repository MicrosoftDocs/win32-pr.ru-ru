---
title: Клокктипе (Чаннелпублишингтипе), элемент
description: Разрешение часов, используемое при записи метки времени для каждого события.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- Журнал событий элемента Клокктипе
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414904"
---
# <a name="clocktype-channelpublishingtype-element"></a><span data-ttu-id="07747-104">Клокктипе (Чаннелпублишингтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="07747-104">clockType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="07747-105">Разрешение часов, используемое при записи метки времени для каждого события.</span><span class="sxs-lookup"><span data-stu-id="07747-105">The clock resolution to use when logging the time stamp for each event.</span></span>

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="07747-106">Элемент **клокктипе** определяется сложным типом [**чаннелпублишингтипе**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="07747-106">The **clockType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="07747-107">Требования</span><span class="sxs-lookup"><span data-stu-id="07747-107">Requirements</span></span>



| <span data-ttu-id="07747-108">Требование</span><span class="sxs-lookup"><span data-stu-id="07747-108">Requirement</span></span> | <span data-ttu-id="07747-109">Значение</span><span class="sxs-lookup"><span data-stu-id="07747-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07747-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07747-110">Minimum supported client</span></span><br/> | <span data-ttu-id="07747-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07747-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07747-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07747-112">Minimum supported server</span></span><br/> | <span data-ttu-id="07747-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07747-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07747-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07747-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="07747-115">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="07747-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="07747-116">**Публикация (Чаннелтипе)**</span><span class="sxs-lookup"><span data-stu-id="07747-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





