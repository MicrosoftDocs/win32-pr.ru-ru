---
title: неподписанный атрибут
description: Ключевое слово без знака указывает, что наиболее значимый бит целочисленной переменной представляет бит данных, а не бит со знаком.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- неподписанный атрибут MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105661665"
---
# <a name="unsigned-attribute"></a><span data-ttu-id="8166c-104">неподписанный атрибут</span><span class="sxs-lookup"><span data-stu-id="8166c-104">unsigned attribute</span></span>

<span data-ttu-id="8166c-105">Ключевое слово **без знака** указывает, что наиболее значимый бит целочисленной переменной представляет бит данных, а не бит со знаком.</span><span class="sxs-lookup"><span data-stu-id="8166c-105">The **unsigned** keyword indicates that the most significant bit of an integer variable represents a data bit rather than a signed bit.</span></span>

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="8166c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8166c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8166c-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="8166c-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="8166c-108">Может быть любым из типов [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**int**](int.md), [**Short**](short.md)и [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="8166c-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="8166c-109">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="8166c-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8166c-110">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="8166c-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="8166c-111">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="8166c-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8166c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8166c-112">Remarks</span></span>

<span data-ttu-id="8166c-113">Это ключевое слово является необязательным и может использоваться с любыми символьными и целочисленными типами [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)и [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="8166c-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="8166c-114">При необходимости можно включить ключевое слово [**int**](int.md) после квалификаторов типа **Long**, **Short** и **Small**.</span><span class="sxs-lookup"><span data-stu-id="8166c-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="8166c-115">При использовании параметра компилятора MIDL [**/char**](-char.md)типы символов и целых чисел, отображаемые в IDL-файле без явных ключевых слов Sign, могут отображаться с ключевым словом [**со знаком**](signed.md) или **без знака** в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="8166c-115">When you use the MIDL compiler switch [**/char**](-char.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the [**signed**](signed.md) or **unsigned** keyword in the generated header file.</span></span> <span data-ttu-id="8166c-116">Чтобы избежать путаницы, укажите знак целого числа и символьных типов.</span><span class="sxs-lookup"><span data-stu-id="8166c-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="8166c-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8166c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8166c-118">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="8166c-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="8166c-119">**char**</span><span class="sxs-lookup"><span data-stu-id="8166c-119">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="8166c-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="8166c-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="8166c-121">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="8166c-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8166c-122">**INT**</span><span class="sxs-lookup"><span data-stu-id="8166c-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="8166c-123">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="8166c-123">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="8166c-124">**short**</span><span class="sxs-lookup"><span data-stu-id="8166c-124">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="8166c-125">**входил**</span><span class="sxs-lookup"><span data-stu-id="8166c-125">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="8166c-126">**значительные**</span><span class="sxs-lookup"><span data-stu-id="8166c-126">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="8166c-127">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="8166c-127">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




