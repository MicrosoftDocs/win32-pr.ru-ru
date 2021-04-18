---
title: Сложный тип Басиаппараметерс — свойства соединения
description: Определяет элемент-заполнитель для конкретного типа метода и конфигурации метода.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- Басиаппараметерс сложный тип EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105694370"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a><span data-ttu-id="433e5-104">Сложный тип Басиаппараметерс — свойства соединения</span><span class="sxs-lookup"><span data-stu-id="433e5-104">BaseEapParameters Complex Type - Connection properties</span></span>

<span data-ttu-id="433e5-105">Сложный тип **басиаппараметерс** определяет элемент-заполнитель для конкретного типа метода и конфигурации метода.</span><span class="sxs-lookup"><span data-stu-id="433e5-105">The **BaseEapParameters** complex type defines the placeholder element for method type and method-specific configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="433e5-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="433e5-106">Child elements</span></span>



| <span data-ttu-id="433e5-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="433e5-107">Element</span></span>                                                                            | <span data-ttu-id="433e5-108">Тип</span><span class="sxs-lookup"><span data-stu-id="433e5-108">Type</span></span>    | <span data-ttu-id="433e5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="433e5-109">Description</span></span>                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [<span data-ttu-id="433e5-110">**Тип**</span><span class="sxs-lookup"><span data-stu-id="433e5-110">**Type**</span></span>](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="433e5-111">Целое число</span><span class="sxs-lookup"><span data-stu-id="433e5-111">integer</span></span> | <span data-ttu-id="433e5-112">Здесь можно использовать любой экземпляр схемы.</span><span class="sxs-lookup"><span data-stu-id="433e5-112">Any schema instance is allowed here.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="433e5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="433e5-113">Remarks</span></span>

<span data-ttu-id="433e5-114">В **басиаппараметерс** метод может определять составные элементы.</span><span class="sxs-lookup"><span data-stu-id="433e5-114">In **BaseEapParameters** the method can define the constituent elements.</span></span> <span data-ttu-id="433e5-115">Метод также выполняет проверку схемы для элементов в **басиаппараметерс**.</span><span class="sxs-lookup"><span data-stu-id="433e5-115">The method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

## <a name="requirements"></a><span data-ttu-id="433e5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="433e5-116">Requirements</span></span>



| <span data-ttu-id="433e5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="433e5-117">Requirement</span></span> | <span data-ttu-id="433e5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="433e5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="433e5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="433e5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="433e5-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="433e5-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="433e5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="433e5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="433e5-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="433e5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="433e5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="433e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433e5-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="433e5-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="433e5-125">Схема baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="433e5-125">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





