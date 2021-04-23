---
title: Сложный тип Валуемапвалуетипе
description: Определяет сопоставление между целочисленным значением и строковым значением. | Сложный тип Валуемапвалуетипе
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- Журнал событий сложных типов Валуемапвалуетипе
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 197eb7e402068f541dc5a385eca14a631de2488c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424182"
---
# <a name="valuemapvaluetype-complex-type"></a><span data-ttu-id="0b553-105">Сложный тип Валуемапвалуетипе</span><span class="sxs-lookup"><span data-stu-id="0b553-105">ValueMapValueType Complex Type</span></span>

<span data-ttu-id="0b553-106">Определяет сопоставление между целочисленным значением и строковым значением.</span><span class="sxs-lookup"><span data-stu-id="0b553-106">Defines the mapping between an integer value and a string value.</span></span>

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
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

## <a name="attributes"></a><span data-ttu-id="0b553-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0b553-107">Attributes</span></span>



| <span data-ttu-id="0b553-108">Имя</span><span class="sxs-lookup"><span data-stu-id="0b553-108">Name</span></span>    | <span data-ttu-id="0b553-109">Тип</span><span class="sxs-lookup"><span data-stu-id="0b553-109">Type</span></span>                                                              | <span data-ttu-id="0b553-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0b553-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b553-111">message</span><span class="sxs-lookup"><span data-stu-id="0b553-111">message</span></span> | [<span data-ttu-id="0b553-112">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="0b553-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="0b553-113">Локализованное строковое значение, с которым сопоставляется целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="0b553-113">The localized string value to which the integer value maps.</span></span> <span data-ttu-id="0b553-114">Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.</span><span class="sxs-lookup"><span data-stu-id="0b553-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                              |
| <span data-ttu-id="0b553-115">символ</span><span class="sxs-lookup"><span data-stu-id="0b553-115">symbol</span></span>  | [<span data-ttu-id="0b553-116">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="0b553-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="0b553-117">Символ, используемый для ссылки на карту в приложении.</span><span class="sxs-lookup"><span data-stu-id="0b553-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="0b553-118">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ для создания константы для Map в файле заголовка, создаваемого компилятором.</span><span class="sxs-lookup"><span data-stu-id="0b553-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="0b553-119">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="0b553-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="0b553-120">значение</span><span class="sxs-lookup"><span data-stu-id="0b553-120">value</span></span>   | [<span data-ttu-id="0b553-121">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="0b553-121">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="0b553-122">Целочисленное значение, сопоставляемое со строковым значением.</span><span class="sxs-lookup"><span data-stu-id="0b553-122">The integer value to map to the string value.</span></span><br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a><span data-ttu-id="0b553-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0b553-123">Requirements</span></span>



| <span data-ttu-id="0b553-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0b553-124">Requirement</span></span> | <span data-ttu-id="0b553-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0b553-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0b553-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b553-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b553-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b553-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0b553-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b553-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b553-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b553-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





