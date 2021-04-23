---
title: Элемент соединения (Connections)
description: Определяет каждый параметр конфигурации и связывает его с именем. Элемент Connection является необязательным.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Элемент соединения EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710505"
---
# <a name="connection-connections-element"></a><span data-ttu-id="fbc19-105">Элемент соединения (Connections)</span><span class="sxs-lookup"><span data-stu-id="fbc19-105">Connection (Connections) Element</span></span>

<span data-ttu-id="fbc19-106">Элемент **Connection (Connections)** определяет каждый параметр конфигурации и связывает его с именем.</span><span class="sxs-lookup"><span data-stu-id="fbc19-106">The **Connection (Connections)** element defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="fbc19-107">Элемент **Connection** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fbc19-107">The **Connection** element is optional.</span></span>

``` syntax
<xs:element name="Connection">
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
```

<span data-ttu-id="fbc19-108">Элемент **Connection** определяется элементом [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fbc19-108">The **Connection** element is defined by the [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fbc19-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fbc19-109">Child elements</span></span>



| <span data-ttu-id="fbc19-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="fbc19-110">Element</span></span>                                                                 | <span data-ttu-id="fbc19-111">Тип</span><span class="sxs-lookup"><span data-stu-id="fbc19-111">Type</span></span>   | <span data-ttu-id="fbc19-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fbc19-112">Description</span></span>                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbc19-113">**Протокола**</span><span class="sxs-lookup"><span data-stu-id="fbc19-113">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | <span data-ttu-id="fbc19-114">Определяет элемент конфигурации EAP.</span><span class="sxs-lookup"><span data-stu-id="fbc19-114">Identifies the EAP configuration element.</span></span><br/>                                                                    |
| [<span data-ttu-id="fbc19-115">**Название**</span><span class="sxs-lookup"><span data-stu-id="fbc19-115">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md) | <span data-ttu-id="fbc19-116">строка</span><span class="sxs-lookup"><span data-stu-id="fbc19-116">string</span></span> | <span data-ttu-id="fbc19-117">Захватывает имя определяемого соединения, помогая идентифицировать несколько соединений.</span><span class="sxs-lookup"><span data-stu-id="fbc19-117">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="fbc19-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fbc19-118">Requirements</span></span>



| <span data-ttu-id="fbc19-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fbc19-119">Requirement</span></span> | <span data-ttu-id="fbc19-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fbc19-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fbc19-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbc19-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc19-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbc19-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fbc19-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbc19-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc19-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fbc19-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbc19-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbc19-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="fbc19-126">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="fbc19-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fbc19-127">**Соединения**</span><span class="sxs-lookup"><span data-stu-id="fbc19-127">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

<span data-ttu-id="fbc19-128">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="fbc19-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fbc19-129">**Соединения**</span><span class="sxs-lookup"><span data-stu-id="fbc19-129">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[<span data-ttu-id="fbc19-130">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="fbc19-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fbc19-131">Схема eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fbc19-131">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





