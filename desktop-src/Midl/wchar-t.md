---
title: атрибут wchar_t
description: '\_Ключевое слово WCHAR t обозначает тип расширенных символов.'
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t атрибута MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2020
ms.locfileid: "104069660"
---
# <a name="wchar_t-attribute"></a><span data-ttu-id="7d350-104">\_атрибут WCHAR t</span><span class="sxs-lookup"><span data-stu-id="7d350-104">wchar\_t attribute</span></span>

<span data-ttu-id="7d350-105">Ключевое слово **WCHAR \_ t** обозначает тип расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="7d350-105">The **wchar\_t** keyword designates a wide-character type.</span></span>

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="7d350-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d350-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d350-107">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="7d350-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7d350-108">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="7d350-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="7d350-109">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="7d350-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d350-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d350-110">Remarks</span></span>

<span data-ttu-id="7d350-111">Тип **WCHAR \_ t** определяется MIDL как [**неподписанный**](unsigned.md) [**короткий**](short.md) (16-разрядный) объект данных.</span><span class="sxs-lookup"><span data-stu-id="7d350-111">The **wchar\_t** type is defined by MIDL as an [**unsigned**](unsigned.md) [**short**](short.md) (16-bit) data object.</span></span>

<span data-ttu-id="7d350-112">Компилятор MIDL допускает переопределение **WCHAR \_ t**, но только в том случае, если он согласуется с предыдущим определением.</span><span class="sxs-lookup"><span data-stu-id="7d350-112">The MIDL compiler allows redefinition of **wchar\_t**, but only if it is consistent with the preceding definition.</span></span>

<span data-ttu-id="7d350-113">Тип расширенных символов является одним из предопределенных типов MIDL.</span><span class="sxs-lookup"><span data-stu-id="7d350-113">The wide-character type is one of the predefined types of MIDL.</span></span> <span data-ttu-id="7d350-114">Тип расширенных символов может отображаться как описатель типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (как спецификатор типа возвращаемого значения функции и как спецификатор типа параметра).</span><span class="sxs-lookup"><span data-stu-id="7d350-114">The wide-character type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="7d350-115">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="7d350-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="7d350-116">**\[ Строковый \]** атрибут может быть применен к указателю или массиву типа **WCHAR \_ t**.</span><span class="sxs-lookup"><span data-stu-id="7d350-116">The **\[string\]** attribute can be applied to a pointer or array of type **wchar\_t**.</span></span>

<span data-ttu-id="7d350-117">Используйте символ **L** перед символом или строковой константой, чтобы обозначить константу расширенного типа символа.</span><span class="sxs-lookup"><span data-stu-id="7d350-117">Use the **L** character before a character or a string constant to designate the wide character type constant.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d350-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d350-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d350-119">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="7d350-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="7d350-120">**char**</span><span class="sxs-lookup"><span data-stu-id="7d350-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="7d350-121">**const**</span><span class="sxs-lookup"><span data-stu-id="7d350-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="7d350-122">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="7d350-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7d350-123">**short**</span><span class="sxs-lookup"><span data-stu-id="7d350-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="7d350-124">**определение**</span><span class="sxs-lookup"><span data-stu-id="7d350-124">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="7d350-125">**без знака**</span><span class="sxs-lookup"><span data-stu-id="7d350-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




