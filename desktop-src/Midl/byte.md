---
title: Byte, атрибут
description: Ключевое слово byte задает 8-разрядный элемент данных.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- байтовый атрибут MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105650317"
---
# <a name="byte-attribute"></a><span data-ttu-id="e8c4b-104">Byte, атрибут</span><span class="sxs-lookup"><span data-stu-id="e8c4b-104">byte attribute</span></span>

<span data-ttu-id="e8c4b-105">Ключевое слово **Byte** задает 8-разрядный элемент данных.</span><span class="sxs-lookup"><span data-stu-id="e8c4b-105">The **byte** keyword specifies an 8-bit data item.</span></span>

``` syntax
byte identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="e8c4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8c4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c4b-107">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="e8c4b-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e8c4b-108">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="e8c4b-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="e8c4b-109">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="e8c4b-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8c4b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8c4b-110">Remarks</span></span>

<span data-ttu-id="e8c4b-111">Элемент данных в **байтах** не преобразуется для передачи в сети в качестве типа [**char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="e8c4b-111">A **byte** data item does not undergo any conversion for transmission on the network as a [**char**](char-idl.md) type might.</span></span>

<span data-ttu-id="e8c4b-112">Тип **Byte** является одним из базовых типов языка определения интерфейса (IDL).</span><span class="sxs-lookup"><span data-stu-id="e8c4b-112">The **byte** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="e8c4b-113">Тип **Byte** может отображаться в виде спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора типа "функция-возврат" и спецификатора типа параметра).</span><span class="sxs-lookup"><span data-stu-id="e8c4b-113">The **byte** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="e8c4b-114">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="e8c4b-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e8c4b-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8c4b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c4b-116">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="e8c4b-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e8c4b-117">**char**</span><span class="sxs-lookup"><span data-stu-id="e8c4b-117">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="e8c4b-118">**const**</span><span class="sxs-lookup"><span data-stu-id="e8c4b-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e8c4b-119">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="e8c4b-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e8c4b-120">**определение**</span><span class="sxs-lookup"><span data-stu-id="e8c4b-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




