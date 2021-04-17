---
title: float, атрибут
description: Ключевое слово float обозначает 32-разрядное число с плавающей запятой.
ms.assetid: dfc94378-13a4-4d34-a254-7ff68f4f9d40
keywords:
- атрибут float с плавающей запятой
topic_type:
- apiref
api_name:
- float
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82d298506c5117c0643df8ecea841832d5f923
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681534"
---
# <a name="float-attribute"></a><span data-ttu-id="785a7-104">float, атрибут</span><span class="sxs-lookup"><span data-stu-id="785a7-104">float attribute</span></span>

<span data-ttu-id="785a7-105">Ключевое слово **float** обозначает 32-разрядное число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="785a7-105">The **float** keyword designates a 32-bit floating-point number.</span></span>

``` syntax
float identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="785a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="785a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="785a7-107">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="785a7-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="785a7-108">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="785a7-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="785a7-109">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="785a7-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="785a7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="785a7-110">Remarks</span></span>

<span data-ttu-id="785a7-111">Тип **float** является одним из базовых типов языка определения интерфейса (IDL).</span><span class="sxs-lookup"><span data-stu-id="785a7-111">The **float** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="785a7-112">Тип **float** может отображаться в виде спецификатора типа в объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возвращаемого типа функции и описателя типа параметра).</span><span class="sxs-lookup"><span data-stu-id="785a7-112">The **float** type can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="785a7-113">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="785a7-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="785a7-114">Тип **float** не может использоваться в объявлениях [**const**](const.md) .</span><span class="sxs-lookup"><span data-stu-id="785a7-114">The **float** type cannot appear in [**const**](const.md) declarations.</span></span>

## <a name="see-also"></a><span data-ttu-id="785a7-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="785a7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="785a7-116">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="785a7-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="785a7-117">**Дважды**</span><span class="sxs-lookup"><span data-stu-id="785a7-117">**double**</span></span>](double.md)
</dt> <dt>

[<span data-ttu-id="785a7-118">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="785a7-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="785a7-119">**определение**</span><span class="sxs-lookup"><span data-stu-id="785a7-119">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




