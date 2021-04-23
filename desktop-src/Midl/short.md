---
title: короткий атрибут
description: Ключевое слово short обозначает 16-разрядное целое число.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- короткий атрибут MIDL
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334283"
---
# <a name="short-attribute"></a><span data-ttu-id="98d03-104">короткий атрибут</span><span class="sxs-lookup"><span data-stu-id="98d03-104">short attribute</span></span>

<span data-ttu-id="98d03-105">Ключевое слово **Short** обозначает 16-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="98d03-105">The **short** keyword designates a 16-bit integer.</span></span>

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="98d03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="98d03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98d03-107">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="98d03-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="98d03-108">Указывает один или несколько стандартных деклараторов C, таких как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="98d03-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="98d03-109">(Деклараторы функций и объявления битовых полей не допускаются в структурах, передаваемых в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="98d03-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="98d03-110">Эти деклараторы разрешены в структурах, которые не передаются.) Несколько деклараторов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="98d03-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98d03-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98d03-111">Remarks</span></span>

<span data-ttu-id="98d03-112">Ключевому слову **Short** может предшествовать либо ключевое слово signed [**, либо**](signed.md) ключевое слово [**без знака**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="98d03-112">The **short** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="98d03-113">Ключевое слово [**int**](int.md) является необязательным и может быть опущено.</span><span class="sxs-lookup"><span data-stu-id="98d03-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="98d03-114">В компиляторе MIDL короткое целое подписывается по умолчанию и является синонимом **короткого типа со знаком**.</span><span class="sxs-lookup"><span data-stu-id="98d03-114">To the MIDL compiler, a short integer is signed by default and is synonymous with **signed short int**.</span></span>

<span data-ttu-id="98d03-115">**Короткий** целочисленный тип является одним из базовых типов языка IDL.</span><span class="sxs-lookup"><span data-stu-id="98d03-115">The **short** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="98d03-116">**Короткий** целочисленный тип может отображаться в виде спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возвращаемого типа функции и описателя типа параметра).</span><span class="sxs-lookup"><span data-stu-id="98d03-116">The **short** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="98d03-117">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="98d03-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="98d03-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98d03-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d03-119">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="98d03-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="98d03-120">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="98d03-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="98d03-121">**INT**</span><span class="sxs-lookup"><span data-stu-id="98d03-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="98d03-122">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="98d03-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="98d03-123">**входил**</span><span class="sxs-lookup"><span data-stu-id="98d03-123">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="98d03-124">**значительные**</span><span class="sxs-lookup"><span data-stu-id="98d03-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="98d03-125">**без знака**</span><span class="sxs-lookup"><span data-stu-id="98d03-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




