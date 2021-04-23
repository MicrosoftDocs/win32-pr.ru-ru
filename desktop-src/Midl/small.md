---
title: маленький атрибут
description: Ключевое слово Small обозначает 8-разрядное целое число.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- маленький атрибут MIDL
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411643"
---
# <a name="small-attribute"></a><span data-ttu-id="1d945-104">маленький атрибут</span><span class="sxs-lookup"><span data-stu-id="1d945-104">small attribute</span></span>

<span data-ttu-id="1d945-105">Ключевое слово **Small** обозначает 8-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="1d945-105">The **small** keyword designates an 8-bit integer number.</span></span>

``` syntax
small identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="1d945-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d945-107">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="1d945-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1d945-108">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="1d945-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="1d945-109">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="1d945-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d945-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d945-110">Remarks</span></span>

<span data-ttu-id="1d945-111">Ключевому слову **Small** может предшествовать либо ключевое слово signed [**, либо**](signed.md) ключевое слово [**без знака**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="1d945-111">The **small** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="1d945-112">Ключевое слово [**int**](int.md) является необязательным и может быть опущено.</span><span class="sxs-lookup"><span data-stu-id="1d945-112">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="1d945-113">Для компилятора MIDL небольшое целое число **подписывается** по умолчанию и является синонимом **небольшого числа со знаком**.</span><span class="sxs-lookup"><span data-stu-id="1d945-113">To the MIDL compiler, a small integer is **signed** by default and is synonymous with **signed small int**.</span></span>

<span data-ttu-id="1d945-114">**Малый** целочисленный тип является одним из базовых типов языка IDL.</span><span class="sxs-lookup"><span data-stu-id="1d945-114">The **small** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="1d945-115">**Небольшой** целочисленный тип может отображаться в виде спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возврата функции и спецификатора типа параметра).</span><span class="sxs-lookup"><span data-stu-id="1d945-115">The **small** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="1d945-116">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="1d945-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="1d945-117">Знак **небольшого** типа можно изменить с помощью параметра компилятора MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="1d945-117">The sign of the **small** type can be modified by the MIDL compiler switch [**/char**](-char.md).</span></span> <span data-ttu-id="1d945-118">Чтобы избежать путаницы, укажите знак целочисленного типа с ключевыми словами " [**подписанные**](signed.md) " и " [**без знака**](unsigned.md)".</span><span class="sxs-lookup"><span data-stu-id="1d945-118">To avoid confusion, specify the sign of the integer type with the keywords [**signed**](signed.md) and [**unsigned**](unsigned.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1d945-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d945-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d945-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="1d945-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="1d945-121">**const**</span><span class="sxs-lookup"><span data-stu-id="1d945-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="1d945-122">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="1d945-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="1d945-123">**INT**</span><span class="sxs-lookup"><span data-stu-id="1d945-123">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="1d945-124">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="1d945-124">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="1d945-125">**short**</span><span class="sxs-lookup"><span data-stu-id="1d945-125">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="1d945-126">**входил**</span><span class="sxs-lookup"><span data-stu-id="1d945-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="1d945-127">**без знака**</span><span class="sxs-lookup"><span data-stu-id="1d945-127">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="1d945-128">**определение**</span><span class="sxs-lookup"><span data-stu-id="1d945-128">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




