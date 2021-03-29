---
title: /char, параметр
description: Параметр/Char помогает обеспечить правильную работу компилятора MIDL и компилятора C для всех типов char и Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- MIDL/char Switch
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784239"
---
# <a name="char-switch"></a><span data-ttu-id="dcc3c-104">/char, параметр</span><span class="sxs-lookup"><span data-stu-id="dcc3c-104">/char switch</span></span>

<span data-ttu-id="dcc3c-105">Параметр **/char** помогает обеспечить правильную работу компилятора MIDL и компилятора C для всех типов [**char**](char-idl.md) и [**Small**](small.md) .</span><span class="sxs-lookup"><span data-stu-id="dcc3c-105">The **/char** switch helps to ensure that the MIDL compiler and C compiler operate together correctly for all [**char**](char-idl.md) and [**small**](small.md) types.</span></span>

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a><span data-ttu-id="dcc3c-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="dcc3c-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span data-ttu-id="dcc3c-107"><span id="signed"></span><span id="SIGNED"></span>подписано \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dcc3c-107"><span id="signed"></span><span id="SIGNED"></span>\*\*\*\*signed\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="dcc3c-108">Указывает, что тип C-компилятора по умолчанию для [**char**](char-idl.md) подписывается.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-108">Specifies that the default C-compiler type for [**char**](char-idl.md) is signed.</span></span> <span data-ttu-id="dcc3c-109">Все вхождения **char** , не сопровождаемые спецификацией знака, создаются как char без знака.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-109">All occurrences of **char** not accompanied by a sign specification are generated as unsigned char.</span></span>

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span data-ttu-id="dcc3c-110"><span id="unsigned"></span><span id="UNSIGNED"></span>без подписи \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dcc3c-110"><span id="unsigned"></span><span id="UNSIGNED"></span>\*\*\*\*unsigned\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="dcc3c-111">Указывает, что по умолчанию для [**char**](char-idl.md) используется тип C-Compiler без знака.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-111">Specifies that the default C-compiler type for [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="dcc3c-112">Все использование [**небольшого**](small.md) символа, не сопровождаемого спецификацией знака, формируется небольшим числом со знаком.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-112">All uses of [**small**](small.md) not accompanied by a sign specification are generated as signed small.</span></span>

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span data-ttu-id="dcc3c-113"><span id="ascii7"></span><span id="ASCII7"></span>ascii7 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dcc3c-113"><span id="ascii7"></span><span id="ASCII7"></span>\*\*\*\*ascii7\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="dcc3c-114">Указывает, что все значения [**char**](char-idl.md) должны быть переданы в создаваемые файлы без определенного ключевого слова Sign.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-114">Specifies that all [**char**](char-idl.md) values are to be passed into the generated files without a specific sign keyword.</span></span> <span data-ttu-id="dcc3c-115">Все использование [**небольшого**](small.md) символа, не сопровождаемого спецификацией знака, формируется **небольшими**.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-115">All uses of [**small**](small.md) not accompanied by a sign specification are generated as **small**.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcc3c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcc3c-116">Remarks</span></span>

<span data-ttu-id="dcc3c-117">По определению MIDL- [**символ**](char-idl.md) не подписан.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-117">By definition, MIDL [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="dcc3c-118">"Малый" определяется с точки зрения **char** ( \# Определите маленький символ), а MIDL [**Small**](small.md) имеет подпись.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-118">"Small" is defined in terms of **char** (\#define small char), and MIDL [**small**](small.md) is signed.</span></span>

<span data-ttu-id="dcc3c-119">Параметр **/char** направляет компилятор MIDL для [**указания явных или**](signed.md) [**неподписанных**](unsigned.md) объявлений в создаваемых файлах, когда объявление знака C-компилятора конфликтует с параметром MIDL по умолчанию для этого типа.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-119">The **/char** switch directs the MIDL compiler to specify explicit [**signed**](signed.md) or [**unsigned**](unsigned.md) declarations in the generated files when the C-compiler sign declaration conflicts with the MIDL default for that type.</span></span>

<span data-ttu-id="dcc3c-120">Помните, что компилятор MIDL создает заглушки как исходный код на языке C, который необходимо компилировать как часть программ клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-120">Remember that the MIDL compiler generates the stubs as C source code, which you must compile as part of your client and server programs.</span></span> <span data-ttu-id="dcc3c-121">Некоторые компиляторы используют знак **со знаком** везде, где в исходном коде указаны данные [**char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="dcc3c-121">Some compilers use a **signed char** everywhere [**char**](char-idl.md) data is specified in the source code.</span></span> <span data-ttu-id="dcc3c-122">Исходный код-заглушка, созданный компилятором MIDL, обрабатывает все данные **типа char** как **неподписанные**.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-122">The stub source code that the MIDL compiler generates treats all **char** data as **unsigned char**.</span></span> <span data-ttu-id="dcc3c-123">Если компилятор MIDL просто создал все данные **char** в IDL-файле как **символьные** данные в заглушках, компиляторы, использующие знак **char** для данных **типа char** , приведут к конфликту в исходном коде заглушки.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-123">If the MIDL compiler simply generated all **char** data in the IDL file as **char** data in the stubs, compilers that use a **signed char** for **char** data would cause a conflict in the stub source code.</span></span>

<span data-ttu-id="dcc3c-124">Параметр командной строки **/char** предназначен для устранения этих потенциальных конфликтов.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-124">The purpose of the **/char** command line switch is to resolve these potential conflicts.</span></span> <span data-ttu-id="dcc3c-125">Он сохраняет все данные, указанные как [**char**](char-idl.md) в IDL-файле, в исходном коде заглушки как **символы без знака** .</span><span class="sxs-lookup"><span data-stu-id="dcc3c-125">It preserves all data specified as [**char**](char-idl.md) in the IDL file as **unsigned char** in the stub source code.</span></span> <span data-ttu-id="dcc3c-126">Он также поддерживает [**небольшие**](small.md) данные как подписанные.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-126">It also maintains [**small**](small.md) data as signed.</span></span>

<span data-ttu-id="dcc3c-127">В следующей таблице перечислены сформированные типы.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-127">The following table summarizes the generated types.</span></span>



| <span data-ttu-id="dcc3c-128">MIDL/char, параметр</span><span class="sxs-lookup"><span data-stu-id="dcc3c-128">midl /char option</span></span>       | <span data-ttu-id="dcc3c-129">Созданный тип char</span><span class="sxs-lookup"><span data-stu-id="dcc3c-129">Generated char type</span></span> | <span data-ttu-id="dcc3c-130">Созданный маленький тип</span><span class="sxs-lookup"><span data-stu-id="dcc3c-130">Generated small type</span></span> |
|-------------------------|---------------------|----------------------|
| <span data-ttu-id="dcc3c-131">**MIDL/char со знаком**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-131">**midl /char signed**</span></span>   | <span data-ttu-id="dcc3c-132">**unsigned char**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-132">**unsigned char**</span></span>   | <span data-ttu-id="dcc3c-133">**small**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-133">**small**</span></span>            |
| <span data-ttu-id="dcc3c-134">**MIDL/char без знака**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-134">**midl /char unsigned**</span></span> | <span data-ttu-id="dcc3c-135">**char**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-135">**char**</span></span>            | <span data-ttu-id="dcc3c-136">**малое целое**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-136">**signed small**</span></span>     |
| <span data-ttu-id="dcc3c-137">**MIDL/char ascii7**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-137">**midl /char ascii7**</span></span>   | <span data-ttu-id="dcc3c-138">**char**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-138">**char**</span></span>            | <span data-ttu-id="dcc3c-139">**small**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-139">**small**</span></span>            |



 

<span data-ttu-id="dcc3c-140">Параметр **/char** , подписанный, указывает, что символы типа char и Small-компилятора имеют подпись.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-140">The **/char** signed option indicates that the C-compiler char and small types are signed.</span></span> <span data-ttu-id="dcc3c-141">Чтобы сопоставить значение языка MIDL по умолчанию для **char**, компилятор MIDL должен преобразовать все использование **char** , не сопровождаемое спецификацией знака, в **символ без знака**.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-141">To match the MIDL default for **char**, the MIDL compiler must convert all uses of **char** not accompanied by a sign specification to **unsigned char**.</span></span> <span data-ttu-id="dcc3c-142">[**Небольшой**](small.md) тип не изменяется, так как значение по умолчанию компилятора C-Compiler соответствует стандарту MIDL по умолчанию для **Small**.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-142">The [**small**](small.md) type is not modified because this C-compiler default matches the MIDL default for **small**.</span></span>

<span data-ttu-id="dcc3c-143">Параметр **/char** без знака указывает, что тип [**char**](char-idl.md) C-Compiler не имеет знака.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-143">The **/char** unsigned option indicates that the C-compiler [**char**](char-idl.md) type is unsigned.</span></span> <span data-ttu-id="dcc3c-144">Компилятор MIDL преобразует все варианты использования [**небольшого**](small.md) , а не с помощью спецификации знака для **небольшого** числа **со знаком** .</span><span class="sxs-lookup"><span data-stu-id="dcc3c-144">The MIDL compiler converts all uses of [**small**](small.md) not accompanied by a sign specification to **signed** **small**.</span></span>

<span data-ttu-id="dcc3c-145">Параметр ascii7 указывает, что в типы [**char**](char-idl.md) не добавляется явная спецификация знака.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-145">The ascii7 option indicates that no explicit sign specification is added to [**char**](char-idl.md) types.</span></span> <span data-ttu-id="dcc3c-146">Тип [**Small**](small.md) создается как **малый**.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-146">The type [**small**](small.md) is generated as **small**.</span></span>

<span data-ttu-id="dcc3c-147">Во избежание путаницы следует по возможности использовать явные спецификации знака для [**char**](char-idl.md) и Small types в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-147">To avoid confusion, you should use explicit sign specifications for [**char**](char-idl.md) and small types whenever possible in the IDL file.</span></span> <span data-ttu-id="dcc3c-148">Обратите внимание, что использование явно подписанных типов **char** в IDL-файле не поддерживается с помощью устройства DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-148">Note that the use of explicitly signed **char** types in your IDL file is not supported by DCE IDL.</span></span> <span data-ttu-id="dcc3c-149">Поэтому эта функция недоступна при компиляции с помощью параметра MIDL [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="dcc3c-149">Therefore, this feature is not available when you compile with the MIDL [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="dcc3c-150">Дополнительные сведения о **/char** см. в разделе [**малый**](small.md).</span><span class="sxs-lookup"><span data-stu-id="dcc3c-150">For more information related to **/char**, see [**small**](small.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dcc3c-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="dcc3c-151">Examples</span></span>

<span data-ttu-id="dcc3c-152">**MIDL/char подписанное имя файла. idl**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-152">**midl /char signed filename.idl**</span></span>

<span data-ttu-id="dcc3c-153">**MIDL/char без знака filename. idl**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-153">**midl /char unsigned filename.idl**</span></span>

<span data-ttu-id="dcc3c-154">**MIDL/char ascii7 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-154">**midl /char ascii7 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="dcc3c-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcc3c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc3c-156">**char**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-156">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="dcc3c-157">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="dcc3c-157">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="dcc3c-158">**/осф**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-158">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="dcc3c-159">**значительные**</span><span class="sxs-lookup"><span data-stu-id="dcc3c-159">**small**</span></span>](small.md)
</dt> </dl>

 

 




