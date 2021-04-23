---
title: Элемент User
description: Сведения об элементе User. Этот элемент не используется при использовании устаревших методов через API-интерфейсы EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Элемент пользователя EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793921"
---
# <a name="user-element"></a><span data-ttu-id="09886-105">Элемент User</span><span class="sxs-lookup"><span data-stu-id="09886-105">User Element</span></span>

<span data-ttu-id="09886-106">Элемент **User** не используется при использовании устаревших методов через API-интерфейсы EAPHost.</span><span class="sxs-lookup"><span data-stu-id="09886-106">The **User** element is not used when using legacy methods via the EAPHost APIs.</span></span>

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="09886-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="09886-107">Child elements</span></span>



| <span data-ttu-id="09886-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="09886-108">Element</span></span>                                                  | <span data-ttu-id="09886-109">Тип</span><span class="sxs-lookup"><span data-stu-id="09886-109">Type</span></span> | <span data-ttu-id="09886-110">Описание</span><span class="sxs-lookup"><span data-stu-id="09886-110">Description</span></span>                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="09886-111">**Протокола**</span><span class="sxs-lookup"><span data-stu-id="09886-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md) |      | <span data-ttu-id="09886-112">Захватывает сведения о типе метода и учетных данных, специфичных для метода.</span><span class="sxs-lookup"><span data-stu-id="09886-112">Captures the method type and method specific credential information.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="09886-113">Требования</span><span class="sxs-lookup"><span data-stu-id="09886-113">Requirements</span></span>



| <span data-ttu-id="09886-114">Роль</span><span class="sxs-lookup"><span data-stu-id="09886-114">Role</span></span> | <span data-ttu-id="09886-115">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="09886-115">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="09886-116">Клиент</span><span class="sxs-lookup"><span data-stu-id="09886-116">Client</span></span><br/> | <span data-ttu-id="09886-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09886-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09886-118">Сервер</span><span class="sxs-lookup"><span data-stu-id="09886-118">Server</span></span><br/> | <span data-ttu-id="09886-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09886-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09886-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09886-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09886-121">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="09886-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="09886-122">Схема eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="09886-122">eapuserpropertiesv1 Schema</span></span>](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





