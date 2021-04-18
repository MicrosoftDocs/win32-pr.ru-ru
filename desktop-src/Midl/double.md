---
title: Double, атрибут
description: Ключевое слово Double обозначает 64-разрядное число с плавающей запятой.
ms.assetid: a235e9c5-90b3-4fa4-9154-06511abcccd0
keywords:
- двойной атрибут MIDL
topic_type:
- apiref
api_name:
- double
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f14f4906de9e843c9413411c9d45ba927cc40ee4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532744"
---
# <a name="double-attribute"></a><span data-ttu-id="e02f7-104">Double, атрибут</span><span class="sxs-lookup"><span data-stu-id="e02f7-104">double attribute</span></span>

<span data-ttu-id="e02f7-105">Ключевое слово **Double** обозначает 64-разрядное число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e02f7-105">The **double** keyword designates a 64-bit floating-point number.</span></span>

``` syntax
double identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="e02f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e02f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e02f7-107">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="e02f7-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e02f7-108">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="e02f7-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="e02f7-109">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="e02f7-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e02f7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e02f7-110">Remarks</span></span>

<span data-ttu-id="e02f7-111">Тип **Double** является одним из базовых типов языка определения интерфейса (IDL).</span><span class="sxs-lookup"><span data-stu-id="e02f7-111">The **double** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="e02f7-112">Этот тип может использоваться в качестве спецификатора типа в объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в качестве спецификатора возвращаемого типа функции и описателя типа параметра).</span><span class="sxs-lookup"><span data-stu-id="e02f7-112">This type can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="e02f7-113">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="e02f7-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="e02f7-114">Тип **Double** не может использоваться в объявлениях [**const**](const.md) .</span><span class="sxs-lookup"><span data-stu-id="e02f7-114">The **double** type cannot appear in [**const**](const.md) declarations.</span></span>

## <a name="see-also"></a><span data-ttu-id="e02f7-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e02f7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e02f7-116">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="e02f7-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e02f7-117">**const**</span><span class="sxs-lookup"><span data-stu-id="e02f7-117">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e02f7-118">**сделать**</span><span class="sxs-lookup"><span data-stu-id="e02f7-118">**float**</span></span>](float.md)
</dt> <dt>

[<span data-ttu-id="e02f7-119">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="e02f7-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e02f7-120">**определение**</span><span class="sxs-lookup"><span data-stu-id="e02f7-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




