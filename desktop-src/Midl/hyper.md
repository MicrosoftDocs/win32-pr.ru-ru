---
title: атрибут Hyper
description: Ключевое слово "Hyper" указывает на 64-разрядное целое число, которое может быть объявлено как со знаком, так и без знака.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- атрибут Hyper MIDL
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783606"
---
# <a name="hyper-attribute"></a><span data-ttu-id="3fbe8-104">атрибут Hyper</span><span class="sxs-lookup"><span data-stu-id="3fbe8-104">hyper attribute</span></span>

<span data-ttu-id="3fbe8-105">Ключевое слово " **Hyper** " указывает на 64-разрядное целое число, которое может быть объявлено как со знаком, так и без знака.</span><span class="sxs-lookup"><span data-stu-id="3fbe8-105">The keyword **hyper** indicates a 64-bit integer that can be declared as either signed or unsigned.</span></span>

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="3fbe8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fbe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fbe8-107">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="3fbe8-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3fbe8-108">Указывает один или несколько стандартных деклараторов C, таких как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="3fbe8-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="3fbe8-109">(Деклараторы функций и объявления битовых полей не допускаются в структурах, передаваемых в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="3fbe8-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="3fbe8-110">Эти деклараторы разрешены в структурах, которые не передаются.) Несколько деклараторов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="3fbe8-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fbe8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fbe8-111">Remarks</span></span>

<span data-ttu-id="3fbe8-112">Тип **Hyper** является одним из базовых типов языка определения интерфейса (IDL).</span><span class="sxs-lookup"><span data-stu-id="3fbe8-112">The **hyper** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="3fbe8-113">Тип **Hyper** может отображаться в виде спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возвращаемого типа функции и в качестве описателя типа параметра).</span><span class="sxs-lookup"><span data-stu-id="3fbe8-113">The **hyper** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="3fbe8-114">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="3fbe8-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="3fbe8-115">Для 16-разрядных платформ компилятор MIDL заменяет неподписанные целые числа с помощью **MIDL \_ ухипер**.</span><span class="sxs-lookup"><span data-stu-id="3fbe8-115">For 16-bit platforms, the MIDL compiler replaces unsigned hyper integers with **MIDL\_uhyper**.</span></span> <span data-ttu-id="3fbe8-116">Это позволяет определять интерфейсы с неподписанными целыми числами на платформах, которые не поддерживают непосредственные 64-разрядные целые числа.</span><span class="sxs-lookup"><span data-stu-id="3fbe8-116">This allows interfaces with unsigned hyper integers to be defined on platforms that do not directly support 64-bit integers.</span></span> <span data-ttu-id="3fbe8-117">**MIDL \_ ухипер** определен в файлах заголовков RPC.</span><span class="sxs-lookup"><span data-stu-id="3fbe8-117">**MIDL\_uhyper** is defined in the RPC header files.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="3fbe8-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fbe8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbe8-119">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="3fbe8-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="3fbe8-120">**const**</span><span class="sxs-lookup"><span data-stu-id="3fbe8-120">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="3fbe8-121">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="3fbe8-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3fbe8-122">**определение**</span><span class="sxs-lookup"><span data-stu-id="3fbe8-122">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




