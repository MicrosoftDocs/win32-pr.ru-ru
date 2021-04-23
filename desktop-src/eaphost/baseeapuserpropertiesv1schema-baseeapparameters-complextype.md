---
title: Сложный тип Басиаппараметерс — свойства пользователя
description: Определяет элемент, в котором был указан устаревший метод и учетные данные, зависящие от метода.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105714057"
---
# <a name="baseeapparameters-complex-type---user-properties"></a><span data-ttu-id="2486a-104">Сложный тип Басиаппараметерс — свойства пользователя</span><span class="sxs-lookup"><span data-stu-id="2486a-104">BaseEapParameters Complex Type - User properties</span></span>

<span data-ttu-id="2486a-105">Сложный тип **басиаппараметерс** определяет элемент, в котором был указан устаревший метод, и учетные данные, зависящие от метода.</span><span class="sxs-lookup"><span data-stu-id="2486a-105">The **BaseEapParameters** complex type defines the element that specified the legacy method selected and method-specific credentials.</span></span>

<span data-ttu-id="2486a-106">Метод может определять составные элементы внутри **басиаппараметерс**; метод также выполняет проверку схемы для элементов в **басиаппараметерс**.</span><span class="sxs-lookup"><span data-stu-id="2486a-106">The method can define the constituent elements inside **BaseEapParameters**; the method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="2486a-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2486a-107">Child elements</span></span>



| <span data-ttu-id="2486a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="2486a-108">Element</span></span>                                                                      | <span data-ttu-id="2486a-109">Тип</span><span class="sxs-lookup"><span data-stu-id="2486a-109">Type</span></span>    | <span data-ttu-id="2486a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2486a-110">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2486a-111">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2486a-111">**Type**</span></span>](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="2486a-112">Целое число</span><span class="sxs-lookup"><span data-stu-id="2486a-112">integer</span></span> | <span data-ttu-id="2486a-113">Определяет элемент заполнителя для выбранного типа метода и учетные данные для конкретного метода.</span><span class="sxs-lookup"><span data-stu-id="2486a-113">Defines the placeholder element for the method type selected and method specific credentials.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="2486a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2486a-114">Requirements</span></span>



| <span data-ttu-id="2486a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2486a-115">Requirement</span></span> | <span data-ttu-id="2486a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2486a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2486a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2486a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2486a-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2486a-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2486a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2486a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2486a-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2486a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2486a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2486a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2486a-122">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="2486a-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2486a-123">Схема baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2486a-123">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





