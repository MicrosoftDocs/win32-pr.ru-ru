---
title: Сложный тип Битмапвалуетипе
description: Определяет сопоставление между битовым значением и строковым значением. | Сложный тип Битмапвалуетипе
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- Журнал событий сложных типов Битмапвалуетипе
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000158"
---
# <a name="bitmapvaluetype-complex-type"></a><span data-ttu-id="e18b3-105">Сложный тип Битмапвалуетипе</span><span class="sxs-lookup"><span data-stu-id="e18b3-105">BitMapValueType Complex Type</span></span>

<span data-ttu-id="e18b3-106">Определяет сопоставление между битовым значением и строковым значением.</span><span class="sxs-lookup"><span data-stu-id="e18b3-106">Defines the mapping between a bit value and a string value.</span></span>

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="e18b3-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e18b3-107">Attributes</span></span>



| <span data-ttu-id="e18b3-108">Имя</span><span class="sxs-lookup"><span data-stu-id="e18b3-108">Name</span></span>    | <span data-ttu-id="e18b3-109">Тип</span><span class="sxs-lookup"><span data-stu-id="e18b3-109">Type</span></span>                                                              | <span data-ttu-id="e18b3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e18b3-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e18b3-111">message</span><span class="sxs-lookup"><span data-stu-id="e18b3-111">message</span></span> | [<span data-ttu-id="e18b3-112">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="e18b3-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="e18b3-113">Локализованное строковое значение, с которым сопоставляется битовое значение.</span><span class="sxs-lookup"><span data-stu-id="e18b3-113">The localized string value to which the bit value maps.</span></span> <span data-ttu-id="e18b3-114">Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.</span><span class="sxs-lookup"><span data-stu-id="e18b3-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                  |
| <span data-ttu-id="e18b3-115">символ</span><span class="sxs-lookup"><span data-stu-id="e18b3-115">symbol</span></span>  | [<span data-ttu-id="e18b3-116">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="e18b3-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="e18b3-117">Символ, используемый для ссылки на карту в приложении.</span><span class="sxs-lookup"><span data-stu-id="e18b3-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="e18b3-118">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ для создания константы для Map в файле заголовка, создаваемого компилятором.</span><span class="sxs-lookup"><span data-stu-id="e18b3-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="e18b3-119">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="e18b3-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="e18b3-120">значение</span><span class="sxs-lookup"><span data-stu-id="e18b3-120">value</span></span>   | [<span data-ttu-id="e18b3-121">**HexInt32Type**</span><span class="sxs-lookup"><span data-stu-id="e18b3-121">**HexInt32Type**</span></span>](eventmanifestschema-hex32type-simpletype.md)  | <span data-ttu-id="e18b3-122">Битовое значение, сопоставляемое со строковым значением.</span><span class="sxs-lookup"><span data-stu-id="e18b3-122">The bit value to map to the string value.</span></span> <span data-ttu-id="e18b3-123">Необходимо указать шестнадцатеричное число, для которого задан один бит.</span><span class="sxs-lookup"><span data-stu-id="e18b3-123">You must specify a hexadecimal number that has a single bit set.</span></span><br/>                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="e18b3-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e18b3-124">Remarks</span></span>

<span data-ttu-id="e18b3-125">Сопоставляет шестнадцатеричное значение (перед числом должно стоять 0x) с одним битом, равным имени.</span><span class="sxs-lookup"><span data-stu-id="e18b3-125">Maps a hexadecimal value (the number must be preceded by 0x) with a single bit set to a name.</span></span>

## <a name="requirements"></a><span data-ttu-id="e18b3-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e18b3-126">Requirements</span></span>



| <span data-ttu-id="e18b3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e18b3-127">Requirement</span></span> | <span data-ttu-id="e18b3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e18b3-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e18b3-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e18b3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e18b3-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e18b3-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e18b3-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e18b3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e18b3-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e18b3-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





