---
title: атрибут LCID
description: Атрибут \ LCID \ задает идентификатор локали и включает поддержку компилятора MIDL, зависящую от языкового стандарта.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- атрибут LCID MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789972"
---
# <a name="lcid-attribute"></a><span data-ttu-id="b711d-104">атрибут LCID</span><span class="sxs-lookup"><span data-stu-id="b711d-104">lcid attribute</span></span>

<span data-ttu-id="b711d-105">Атрибут **\[ LCID \]** задает идентификатор локали и включает поддержку компилятора MIDL, зависящую от языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="b711d-105">The **\[lcid\]** attribute specifies a locale identifier and enables locale-specific MIDL compiler support.</span></span>

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="b711d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b711d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b711d-107">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="b711d-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="b711d-108">Задает универсальный уникальный идентификационный номер для [**библиотеки**](library.md).</span><span class="sxs-lookup"><span data-stu-id="b711d-108">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="b711d-109">*localeID*</span><span class="sxs-lookup"><span data-stu-id="b711d-109">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="b711d-110">Указывает 32-разрядный идентификатор локали, используемый в поддержке национальных языков Windows.</span><span class="sxs-lookup"><span data-stu-id="b711d-110">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="b711d-111">Обычно идентификатор локали указывается в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="b711d-111">Typically the locale identifier is given in hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="b711d-112">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="b711d-112">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b711d-113">Ноль или более атрибутов, которые необходимо применить к [**библиотеке**](library.md).</span><span class="sxs-lookup"><span data-stu-id="b711d-113">Zero or more attributes to apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="b711d-114">*имя библиотеки*</span><span class="sxs-lookup"><span data-stu-id="b711d-114">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b711d-115">Имя, по которому программные компоненты ссылаются на [**библиотеку**](library.md).</span><span class="sxs-lookup"><span data-stu-id="b711d-115">The name by which software components refer to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="b711d-116">*Library-операторы определения*</span><span class="sxs-lookup"><span data-stu-id="b711d-116">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="b711d-117">Одна или несколько инструкций MIDL, которые определяют содержимое [**библиотеки**](library.md).</span><span class="sxs-lookup"><span data-stu-id="b711d-117">One or more MIDL statements which define the contents of the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="b711d-118">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="b711d-118">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b711d-119">Указывает имя функции в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="b711d-119">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="b711d-120">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="b711d-120">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b711d-121">Ноль или несколько атрибутов MIDL, которые будут применены к параметру функции.</span><span class="sxs-lookup"><span data-stu-id="b711d-121">Zero or more MIDL attributes that will be applied to the function parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b711d-122">*имя параметра*</span><span class="sxs-lookup"><span data-stu-id="b711d-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b711d-123">Задает имя параметра в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="b711d-123">Specifies the name of the parameter in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b711d-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b711d-124">Remarks</span></span>

<span data-ttu-id="b711d-125">Синтаксис **\[ LCID \]** имеет две различные формы. воздействие атрибута зависит от того, какой синтаксис используется — синтаксис инструкции [**библиотеки**](library.md) или синтаксис параметра.</span><span class="sxs-lookup"><span data-stu-id="b711d-125">The **\[lcid\]** syntax has two different forms; the effect of the attribute depends on which syntax you use — either the [**library**](library.md) statement syntax or the parameter syntax.</span></span>

<span data-ttu-id="b711d-126">При применении к оператору [**Library**](library.md) вместе с аргументом LocaleID, как показано в первом примере, атрибут **\[ LCID \]** определяет языковой стандарт для библиотеки типов или аргумента функции и позволяет использовать международные символы внутри блока Library.</span><span class="sxs-lookup"><span data-stu-id="b711d-126">When applied to the [**library**](library.md) statement, along with a localeID argument, as shown in the first example, the **\[lcid\]** attribute identifies the locale for a type library or for a function argument and lets you use international characters inside the library block.</span></span>

<span data-ttu-id="b711d-127">Начиная с версии 3.01.75 компилятора MIDL идентификатор языкового стандарта, предоставляемый этим атрибутом, не только добавляет в итоговую библиотеку типов, но и изменяет поведение компилятора.</span><span class="sxs-lookup"><span data-stu-id="b711d-127">Effective with version 3.01.75 of the MIDL compiler, the locale identifier supplied by this attribute not only decorates the resulting type library, but actually changes the behavior of the compiler.</span></span> <span data-ttu-id="b711d-128">В операторе [**Library**](library.md) с точки, где используется атрибут **\[ LCID \]** , MIDL принимает входные данные, локализованные в соответствии с заданным языковым стандартом.</span><span class="sxs-lookup"><span data-stu-id="b711d-128">Within a [**library**](library.md) statement, from the point where the **\[lcid\]** attribute is used, MIDL will accept input localized according to the specified locale.</span></span> <span data-ttu-id="b711d-129">В частности, доступна полная поддержка азиатских языков, таких как японский, китайский и Корейский (полная поддержка DBCS).</span><span class="sxs-lookup"><span data-stu-id="b711d-129">In particular, full support for Asian languages such as Japanese, Chinese and Korean (full DBCS support) is available.</span></span> <span data-ttu-id="b711d-130">Ниже перечислены функции, поддерживаемые локализацией: комментарии, строки, хелпстрингс и идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="b711d-130">Features supported by the localization are: comments, strings, helpstrings and identifiers.</span></span>

<span data-ttu-id="b711d-131">Используйте параметр компилятора [**/LCID**](-lcid.md) , чтобы обеспечить доступность этой поддержки локализации для всего входного файла, включая имя файла и путь к каталогу, а не только внутри блока библиотеки.</span><span class="sxs-lookup"><span data-stu-id="b711d-131">Use the [**/lcid**](-lcid.md) compiler switch to have this localization support available to the entire input file, including file name and directory path, rather than just inside the library block.</span></span>

<span data-ttu-id="b711d-132">При применении к параметру атрибут **\[ LCID \]** позволяет передать в функцию идентификатор локали, как показано во втором примере.</span><span class="sxs-lookup"><span data-stu-id="b711d-132">When applied to a parameter, the **\[lcid\]** attribute lets you pass a locale identifier to a function, as shown in the second example.</span></span> <span data-ttu-id="b711d-133">К параметрам **\[ LCID \]** применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="b711d-133">The following restrictions apply to **\[lcid\]** parameters:</span></span>

-   <span data-ttu-id="b711d-134">Функция может иметь не более одного параметра **\[ LCID \]** .</span><span class="sxs-lookup"><span data-stu-id="b711d-134">A function can have at most one **\[lcid\]** parameter.</span></span>
-   <span data-ttu-id="b711d-135">Тип данных параметра должен быть [**длинным**](long.md).</span><span class="sxs-lookup"><span data-stu-id="b711d-135">The data type of the parameter must be [**long**](long.md).</span></span>
-   <span data-ttu-id="b711d-136">Направление параметра должно быть **\[** [](in.md) **\]** только в.</span><span class="sxs-lookup"><span data-stu-id="b711d-136">The direction of the parameter must be **\[**[**in**](in.md)**\]** only.</span></span>
-   <span data-ttu-id="b711d-137">Параметр **\[ LCID \]** должен следовать за любыми другими параметрами, кроме **\[** [](retval.md) **\]** параметра retval.</span><span class="sxs-lookup"><span data-stu-id="b711d-137">The **\[lcid\]** parameter must follow any other parameters, except a **\[**[**retval**](retval.md)**\]** parameter.</span></span>
-   <span data-ttu-id="b711d-138">Атрибут **\[ LCID \]** нельзя применить к [**DISP-интерфейсу**](dispinterface.md) или параметру [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="b711d-138">You cannot apply the **\[lcid\]** attribute to a [**dispinterface**](dispinterface.md) or [**coclass**](coclass.md) parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="b711d-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="b711d-139">Examples</span></span>

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a><span data-ttu-id="b711d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b711d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b711d-141">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="b711d-141">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="b711d-142">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="b711d-142">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="b711d-143">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="b711d-143">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b711d-144">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="b711d-144">**/lcid**</span></span>](-lcid.md)
</dt> <dt>

[<span data-ttu-id="b711d-145">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="b711d-145">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="b711d-146">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="b711d-146">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b711d-147">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="b711d-147">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b711d-148">**retval**</span><span class="sxs-lookup"><span data-stu-id="b711d-148">**retval**</span></span>](retval.md)
</dt> </dl>

 

 