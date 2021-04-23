---
title: атрибут со знаком
description: Ключевое слово с подписью указывает, что наиболее значимый бит целочисленной переменной представляет бит знака, а не бит данных.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- подписанный атрибут MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889320"
---
# <a name="signed-attribute"></a><span data-ttu-id="e3e12-104">атрибут со знаком</span><span class="sxs-lookup"><span data-stu-id="e3e12-104">signed attribute</span></span>

<span data-ttu-id="e3e12-105">Ключевое слово с **подписью** указывает, что наиболее значимый бит целочисленной переменной представляет бит знака, а не бит данных.</span><span class="sxs-lookup"><span data-stu-id="e3e12-105">The **signed** keyword indicates the most significant bit of an integer variable represents a sign bit rather than a data bit.</span></span>

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="e3e12-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3e12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e12-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="e3e12-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e12-108">Может быть любой из типов [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)и [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="e3e12-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3e12-109">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="e3e12-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e12-110">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="e3e12-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="e3e12-111">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="e3e12-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3e12-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3e12-112">Remarks</span></span>

<span data-ttu-id="e3e12-113">Это ключевое слово является необязательным и может использоваться с любыми символьными и целочисленными типами [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)и [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="e3e12-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="e3e12-114">При необходимости можно включить ключевое слово [**int**](int.md) после квалификаторов типа **Long**, **Short** и **Small**.</span><span class="sxs-lookup"><span data-stu-id="e3e12-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="e3e12-115">При использовании целочисленного параметра компилятора MIDL типы [**char**](char-idl.md), Character и Integer, которые ОТОБРАЖАЮТСЯ в IDL-файле без явных ключевых слов Sign, могут появляться с **подписанными** или [**неподписанными**](unsigned.md) ключевыми словами в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="e3e12-115">When you use the MIDL compiler switch [**char**](char-idl.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the **signed** or [**unsigned**](unsigned.md) keywords in the generated header file.</span></span> <span data-ttu-id="e3e12-116">Чтобы избежать путаницы, укажите знак целого числа и символьных типов.</span><span class="sxs-lookup"><span data-stu-id="e3e12-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3e12-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3e12-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e12-118">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="e3e12-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e3e12-119">**/Char**</span><span class="sxs-lookup"><span data-stu-id="e3e12-119">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="e3e12-120">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="e3e12-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e3e12-121">**INT**</span><span class="sxs-lookup"><span data-stu-id="e3e12-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="e3e12-122">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="e3e12-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="e3e12-123">**short**</span><span class="sxs-lookup"><span data-stu-id="e3e12-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="e3e12-124">**значительные**</span><span class="sxs-lookup"><span data-stu-id="e3e12-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="e3e12-125">**без знака**</span><span class="sxs-lookup"><span data-stu-id="e3e12-125">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="e3e12-126">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="e3e12-126">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




