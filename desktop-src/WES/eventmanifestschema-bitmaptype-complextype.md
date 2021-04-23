---
title: Сложный тип Битмаптипе
description: Определяет список сопоставлений имен и значений между битовыми значениями и строковыми значениями.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- Журнал событий сложных типов Битмаптипе
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493107"
---
# <a name="bitmaptype-complex-type"></a><span data-ttu-id="5a873-104">Сложный тип Битмаптипе</span><span class="sxs-lookup"><span data-stu-id="5a873-104">BitMapType Complex Type</span></span>

<span data-ttu-id="5a873-105">Определяет список сопоставлений имен и значений между битовыми значениями и строковыми значениями.</span><span class="sxs-lookup"><span data-stu-id="5a873-105">Defines a list of name/value mappings between bit values and string values.</span></span>

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5a873-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5a873-106">Child elements</span></span>



| <span data-ttu-id="5a873-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="5a873-107">Element</span></span>                                                   | <span data-ttu-id="5a873-108">Тип</span><span class="sxs-lookup"><span data-stu-id="5a873-108">Type</span></span>                                                                       | <span data-ttu-id="5a873-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5a873-109">Description</span></span>                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="5a873-110">**Таблица**</span><span class="sxs-lookup"><span data-stu-id="5a873-110">**map**</span></span>](eventmanifestschema-map-bitmaptype-element.md) | [<span data-ttu-id="5a873-111">**битмапвалуетипе**</span><span class="sxs-lookup"><span data-stu-id="5a873-111">**BitMapValueType**</span></span>](eventmanifestschema-bitmapvaluetype-complextype.md) | <span data-ttu-id="5a873-112">Определяет сопоставление между битовым значением и строковым значением.</span><span class="sxs-lookup"><span data-stu-id="5a873-112">Defines the mapping between a bit value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="5a873-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5a873-113">Attributes</span></span>



| <span data-ttu-id="5a873-114">Имя</span><span class="sxs-lookup"><span data-stu-id="5a873-114">Name</span></span>   | <span data-ttu-id="5a873-115">Тип</span><span class="sxs-lookup"><span data-stu-id="5a873-115">Type</span></span>                                                              | <span data-ttu-id="5a873-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5a873-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a873-117">name</span><span class="sxs-lookup"><span data-stu-id="5a873-117">name</span></span>   | <span data-ttu-id="5a873-118">строка</span><span class="sxs-lookup"><span data-stu-id="5a873-118">string</span></span>                                                            | <span data-ttu-id="5a873-119">Имя битовой карты.</span><span class="sxs-lookup"><span data-stu-id="5a873-119">The name of the bitmap.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5a873-120">символ</span><span class="sxs-lookup"><span data-stu-id="5a873-120">symbol</span></span> | [<span data-ttu-id="5a873-121">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="5a873-121">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="5a873-122">Символ, используемый для ссылки на сопоставления в приложении.</span><span class="sxs-lookup"><span data-stu-id="5a873-122">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="5a873-123">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ для создания константы для Map в файле заголовка, создаваемого компилятором.</span><span class="sxs-lookup"><span data-stu-id="5a873-123">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="5a873-124">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="5a873-124">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5a873-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5a873-125">Requirements</span></span>



| <span data-ttu-id="5a873-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5a873-126">Requirement</span></span> | <span data-ttu-id="5a873-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5a873-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a873-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a873-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5a873-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a873-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a873-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a873-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5a873-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a873-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





