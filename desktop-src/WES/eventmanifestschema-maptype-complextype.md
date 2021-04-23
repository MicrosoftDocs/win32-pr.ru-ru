---
title: Сложный тип Маптипе
description: Определяет список пар "имя-значение".
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- Журнал событий сложных типов Маптипе
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801444"
---
# <a name="maptype-complex-type"></a><span data-ttu-id="a605f-104">Сложный тип Маптипе</span><span class="sxs-lookup"><span data-stu-id="a605f-104">MapType Complex Type</span></span>

<span data-ttu-id="a605f-105">Определяет список пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="a605f-105">Defines a list of name/value pairs.</span></span>

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a605f-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a605f-106">Child elements</span></span>



| <span data-ttu-id="a605f-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a605f-107">Element</span></span>                                                          | <span data-ttu-id="a605f-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a605f-108">Type</span></span>                                                                 | <span data-ttu-id="a605f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a605f-109">Description</span></span>                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a605f-110">**Массив**</span><span class="sxs-lookup"><span data-stu-id="a605f-110">**bitMap**</span></span>](eventmanifestschema-bitmap-maptype-element.md)     | [<span data-ttu-id="a605f-111">**битмаптипе**</span><span class="sxs-lookup"><span data-stu-id="a605f-111">**BitMapType**</span></span>](eventmanifestschema-bitmaptype-complextype.md)     | <span data-ttu-id="a605f-112">Определяет список пар "имя-значение", которые сопоставляют битовые значения и строковые значения.</span><span class="sxs-lookup"><span data-stu-id="a605f-112">Defines a list of name/value pairs that map bit values and string values.</span></span><br/>     |
| [<span data-ttu-id="a605f-113">**valueMap**</span><span class="sxs-lookup"><span data-stu-id="a605f-113">**valueMap**</span></span>](eventmanifestschema-valuemap-maptype-element.md) | [<span data-ttu-id="a605f-114">**валуемаптипе**</span><span class="sxs-lookup"><span data-stu-id="a605f-114">**ValueMapType**</span></span>](eventmanifestschema-valuemaptype-complextype.md) | <span data-ttu-id="a605f-115">Определяет список пар "имя-значение", которые сопоставляют целочисленные значения и строковые значения.</span><span class="sxs-lookup"><span data-stu-id="a605f-115">Defines a list of name/value pairs that map integer values and string values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a605f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a605f-116">Remarks</span></span>

<span data-ttu-id="a605f-117">Как правило, карты создаются для предоставления перечисленных строковых значений для данных событий.</span><span class="sxs-lookup"><span data-stu-id="a605f-117">Typically, you create maps to provide enumerated string values for event data.</span></span>

## <a name="examples"></a><span data-ttu-id="a605f-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="a605f-118">Examples</span></span>

<span data-ttu-id="a605f-119">В следующем примере показано, как указать карту значений и битовую карту.</span><span class="sxs-lookup"><span data-stu-id="a605f-119">The following example shows how to specify a value map and bitmap.</span></span>


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a><span data-ttu-id="a605f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a605f-120">Requirements</span></span>



| <span data-ttu-id="a605f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a605f-121">Requirement</span></span> | <span data-ttu-id="a605f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a605f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a605f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a605f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a605f-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a605f-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a605f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a605f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a605f-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a605f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





