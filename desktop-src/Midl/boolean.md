---
title: логический атрибут
description: Ключевое слово Boolean указывает, что выражение или константное выражение, связанное с идентификатором, принимает только значения TRUE и FALSE.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- логический атрибут MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411865"
---
# <a name="boolean-attribute"></a><span data-ttu-id="38d3a-104">логический атрибут</span><span class="sxs-lookup"><span data-stu-id="38d3a-104">boolean attribute</span></span>

<span data-ttu-id="38d3a-105">Ключевое слово **Boolean** указывает, что выражение или константное выражение, связанное с идентификатором, принимает только значения **true** и **false**.</span><span class="sxs-lookup"><span data-stu-id="38d3a-105">The keyword **boolean** indicates that the expression or constant expression associated with the identifier takes only the values **TRUE** and **FALSE**.</span></span>

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="38d3a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38d3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d3a-107">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="38d3a-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="38d3a-108">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="38d3a-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="38d3a-109">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="38d3a-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38d3a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38d3a-110">Remarks</span></span>

<span data-ttu-id="38d3a-111">**Логический** тип является одним из базовых типов языка IDL.</span><span class="sxs-lookup"><span data-stu-id="38d3a-111">The **boolean** type is one of the base types of the IDL language.</span></span> <span data-ttu-id="38d3a-112">**Логический** тип может использоваться в качестве спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возвращаемого типа функции и в качестве описателя типа параметра).</span><span class="sxs-lookup"><span data-stu-id="38d3a-112">The **boolean** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="38d3a-113">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="38d3a-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="38d3a-114">Базовый тип **Boolean** несовместим с атрибутом [**oleautomation**](oleautomation.md) .</span><span class="sxs-lookup"><span data-stu-id="38d3a-114">The **boolean** base type is not compatible with the [**oleautomation**](oleautomation.md) attribute.</span></span> <span data-ttu-id="38d3a-115">Используйте вариант \_ bool в интерфейсах, совместимых с автоматизацией.</span><span class="sxs-lookup"><span data-stu-id="38d3a-115">Use VARIANT\_BOOL in your Automation-compatible interfaces.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="38d3a-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38d3a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d3a-117">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="38d3a-117">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="38d3a-118">**const**</span><span class="sxs-lookup"><span data-stu-id="38d3a-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="38d3a-119">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="38d3a-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="38d3a-120">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="38d3a-120">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="38d3a-121">**определение**</span><span class="sxs-lookup"><span data-stu-id="38d3a-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




