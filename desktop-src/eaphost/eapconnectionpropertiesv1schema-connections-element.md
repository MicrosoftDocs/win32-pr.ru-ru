---
title: Connections, элемент
description: Сведения об элементе Connections. Этот элемент собирает и содержит ноль или более элементов соединения.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Элемент Connections EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105710356"
---
# <a name="connections-element"></a><span data-ttu-id="b47fa-105">Connections, элемент</span><span class="sxs-lookup"><span data-stu-id="b47fa-105">Connections Element</span></span>

<span data-ttu-id="b47fa-106">Элемент **Connections** собирает и содержит ноль или более элементов [**соединения**](eapconnectionpropertiesv1schema-connection-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b47fa-106">The **Connections** element collects and contains zero or more [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) elements.</span></span>

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Name"
                            type="string"
                         />
                        <xs:element
                            maxOccurs="unbounded"
                            ref="Eap"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="b47fa-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b47fa-107">Child elements</span></span>



| <span data-ttu-id="b47fa-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="b47fa-108">Element</span></span>                                                                              | <span data-ttu-id="b47fa-109">Тип</span><span class="sxs-lookup"><span data-stu-id="b47fa-109">Type</span></span>   | <span data-ttu-id="b47fa-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b47fa-110">Description</span></span>                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b47fa-111">**Протокола**</span><span class="sxs-lookup"><span data-stu-id="b47fa-111">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | <span data-ttu-id="b47fa-112">Определяет элемент конфигурации EAP.</span><span class="sxs-lookup"><span data-stu-id="b47fa-112">Identifies the EAP configuration element.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="b47fa-113">**Соединен**</span><span class="sxs-lookup"><span data-stu-id="b47fa-113">**Connection**</span></span>](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | <span data-ttu-id="b47fa-114">Определяет каждый параметр конфигурации и связывает его с именем.</span><span class="sxs-lookup"><span data-stu-id="b47fa-114">Defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="b47fa-115">Элемент [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b47fa-115">The [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="b47fa-116">**Название**</span><span class="sxs-lookup"><span data-stu-id="b47fa-116">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md)              | <span data-ttu-id="b47fa-117">строка</span><span class="sxs-lookup"><span data-stu-id="b47fa-117">string</span></span> | <span data-ttu-id="b47fa-118">Захватывает имя определяемого соединения, помогая идентифицировать несколько соединений.</span><span class="sxs-lookup"><span data-stu-id="b47fa-118">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span><br/>                                                                     |



## <a name="remarks"></a><span data-ttu-id="b47fa-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b47fa-119">Remarks</span></span>

<span data-ttu-id="b47fa-120">Элемент **Connections** не используется с устаревшими методами через API-интерфейсы EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b47fa-120">The **Connections** element is not used with legacy methods via the EAPHost APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b47fa-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b47fa-121">Requirements</span></span>



| <span data-ttu-id="b47fa-122">Роль</span><span class="sxs-lookup"><span data-stu-id="b47fa-122">Role</span></span> | <span data-ttu-id="b47fa-123">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="b47fa-123">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="b47fa-124">Клиент</span><span class="sxs-lookup"><span data-stu-id="b47fa-124">Client</span></span><br/> | <span data-ttu-id="b47fa-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b47fa-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b47fa-126">Сервер</span><span class="sxs-lookup"><span data-stu-id="b47fa-126">Server</span></span><br/> | <span data-ttu-id="b47fa-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b47fa-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b47fa-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b47fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47fa-129">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="b47fa-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b47fa-130">Схема eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b47fa-130">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





