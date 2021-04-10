---
title: char, атрибут
description: Ключевое слово char определяет 8-разрядный элемент данных.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- атрибут char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889828"
---
# <a name="char-attribute"></a><span data-ttu-id="6f123-104">char, атрибут</span><span class="sxs-lookup"><span data-stu-id="6f123-104">char attribute</span></span>

<span data-ttu-id="6f123-105">Ключевое слово **char** определяет 8-разрядный элемент данных.</span><span class="sxs-lookup"><span data-stu-id="6f123-105">The **char** keyword specifies an 8-bit data item.</span></span>

``` syntax
char identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="6f123-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f123-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f123-107">*идентификатор — имя*</span><span class="sxs-lookup"><span data-stu-id="6f123-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6f123-108">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="6f123-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="6f123-109">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="6f123-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f123-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f123-110">Remarks</span></span>

<span data-ttu-id="6f123-111">Ключевое слово **char** определяет элемент данных с 8 битами.</span><span class="sxs-lookup"><span data-stu-id="6f123-111">The keyword **char** identifies a data item that has 8 bits.</span></span> <span data-ttu-id="6f123-112">Для компилятора MIDL **символ** по умолчанию не подписан и является синонимом [**неподписанного**](unsigned.md) **char**.</span><span class="sxs-lookup"><span data-stu-id="6f123-112">To the MIDL compiler, a **char** is unsigned by default and is synonymous with [**unsigned**](unsigned.md) **char**.</span></span>

<span data-ttu-id="6f123-113">В этой версии Microsoft RPC таблицы преобразования символов, выполняющие преобразование между ASCII и EBCDIC, встроены в библиотеки времени выполнения и не могут быть изменены пользователем.</span><span class="sxs-lookup"><span data-stu-id="6f123-113">In this version of Microsoft RPC, the character translation tables that convert between ASCII and EBCDIC are built into the run-time libraries and cannot be changed by the user.</span></span>

<span data-ttu-id="6f123-114">Тип **char** является одним из базовых типов языка определения интерфейса (IDL).</span><span class="sxs-lookup"><span data-stu-id="6f123-114">The **char** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="6f123-115">Тип **char** может отображаться в виде спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возвращаемого типа функции и описателя типа параметра).</span><span class="sxs-lookup"><span data-stu-id="6f123-115">The **char** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="6f123-116">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="6f123-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="6f123-117">Компиляторы DCE IDL не принимают ключевое слово, [**Подписывание**](signed.md) которого было применено к типам **char** .</span><span class="sxs-lookup"><span data-stu-id="6f123-117">DCE IDL compilers do not accept the keyword [**signed**](signed.md) applied to **char** types.</span></span> <span data-ttu-id="6f123-118">Поэтому эта функция недоступна при использовании параметра компилятора MIDL [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="6f123-118">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f123-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f123-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f123-120">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="6f123-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="6f123-121">**byte**</span><span class="sxs-lookup"><span data-stu-id="6f123-121">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="6f123-122">**/Char**</span><span class="sxs-lookup"><span data-stu-id="6f123-122">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="6f123-123">**const**</span><span class="sxs-lookup"><span data-stu-id="6f123-123">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="6f123-124">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="6f123-124">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6f123-125">**/осф**</span><span class="sxs-lookup"><span data-stu-id="6f123-125">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="6f123-126">**входил**</span><span class="sxs-lookup"><span data-stu-id="6f123-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="6f123-127">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6f123-127">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="6f123-128">**определение**</span><span class="sxs-lookup"><span data-stu-id="6f123-128">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="6f123-129">**без знака**</span><span class="sxs-lookup"><span data-stu-id="6f123-129">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="6f123-130">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="6f123-130">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




