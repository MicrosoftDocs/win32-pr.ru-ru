---
description: Маркер среда выполнения Windows строки.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (HString. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682686"
---
# <a name="hstring"></a><span data-ttu-id="3e14d-103">HSTRING</span><span class="sxs-lookup"><span data-stu-id="3e14d-103">HSTRING</span></span>

<span data-ttu-id="3e14d-104">Маркер среда выполнения Windows строки.</span><span class="sxs-lookup"><span data-stu-id="3e14d-104">A handle to a Windows Runtime string.</span></span>


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a><span data-ttu-id="3e14d-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e14d-105">Remarks</span></span>

<span data-ttu-id="3e14d-106">Используйте **HString** для представления неизменяемых строк в среда выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="3e14d-106">Use **HSTRING** to represent immutable strings in the Windows Runtime.</span></span>

<span data-ttu-id="3e14d-107">JavaScript и другие языки, такие как C \# и Microsoft Visual Basic, могут использовать строки, представленные с помощью **HString**.</span><span class="sxs-lookup"><span data-stu-id="3e14d-107">JavaScript and other languages, such as C\#, and Microsoft Visual Basic, can use strings that are represented by using **HSTRING**.</span></span> <span data-ttu-id="3e14d-108">В следующей таблице показано, как **HString** представлен на других языках.</span><span class="sxs-lookup"><span data-stu-id="3e14d-108">The following table shows how an **HSTRING** is represented in other languages.</span></span>



| <span data-ttu-id="3e14d-109">Язык программирования</span><span class="sxs-lookup"><span data-stu-id="3e14d-109">Programming Language</span></span>                                                                    | <span data-ttu-id="3e14d-110">Строковое представление</span><span class="sxs-lookup"><span data-stu-id="3e14d-110">String Representation</span></span>                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="3e14d-111">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="3e14d-111">C++/WinRT</span></span>](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | <span data-ttu-id="3e14d-112">класс [WinRT:: HString](/uwp/cpp-ref-for-winrt/hstring)</span><span class="sxs-lookup"><span data-stu-id="3e14d-112">[winrt::hstring](/uwp/cpp-ref-for-winrt/hstring) class</span></span>     |
| <span data-ttu-id="3e14d-113">Расширения компонентов Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span><span class="sxs-lookup"><span data-stu-id="3e14d-113">Visual C++ component extensions ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span></span> | <span data-ttu-id="3e14d-114">Класс [Platform:: String](/cpp/cppcx/platform-string-class)</span><span class="sxs-lookup"><span data-stu-id="3e14d-114">[Platform::String](/cpp/cppcx/platform-string-class) class</span></span> |
| <span data-ttu-id="3e14d-115">JavaScript</span><span class="sxs-lookup"><span data-stu-id="3e14d-115">JavaScript</span></span>                                                                              | <span data-ttu-id="3e14d-116">String - объект</span><span class="sxs-lookup"><span data-stu-id="3e14d-116">String object</span></span>                                              |
| <span data-ttu-id="3e14d-117">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="3e14d-117">.NET Framework</span></span>                                                                          | <span data-ttu-id="3e14d-118">Класс System. String</span><span class="sxs-lookup"><span data-stu-id="3e14d-118">System.String class</span></span>                                        |



 

<span data-ttu-id="3e14d-119">Обработчик **HString** является стандартным типом обработчика.</span><span class="sxs-lookup"><span data-stu-id="3e14d-119">The **HSTRING** handle is a standard handle type.</span></span> <span data-ttu-id="3e14d-120">Семантически, **HString** , содержащий значение **null** , представляет пустую строку, которая состоит из нулевых символов содержимого и завершающего **нуль** -символа.</span><span class="sxs-lookup"><span data-stu-id="3e14d-120">Semantically, an **HSTRING** containing the value **NULL** represents the empty string, which consists of zero content characters and a terminating **NULL** character.</span></span> <span data-ttu-id="3e14d-121">Создание строки через [**виндовскреатестринг**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) с нулевым числом символов приведет к созданию значения **null** для этого обработчика.</span><span class="sxs-lookup"><span data-stu-id="3e14d-121">Creating a string via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) with zero characters will produce the handle value **NULL**.</span></span> <span data-ttu-id="3e14d-122">При вызове [**виндовсжетстрингравбуффер**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) со значением **null** возвращается указатель на пустую строку, за которым следует только завершающий символ **nul** .</span><span class="sxs-lookup"><span data-stu-id="3e14d-122">When calling [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) with the value **NULL**, a pointer to an empty string followed only by the **NUL** terminating character will be returned.</span></span> <span data-ttu-id="3e14d-123">Не существует уникального значения, представляющего неинициализированный **HString** .</span><span class="sxs-lookup"><span data-stu-id="3e14d-123">No distinct value exists to represent an **HSTRING** that is uninitialized.</span></span>

<span data-ttu-id="3e14d-124">Вызовите функцию [**виндовскреатестринг**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) , чтобы создать новый **HString**, и вызовите функцию [**виндовсделетестринг**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) для освобождения ссылки на память резервной строки.</span><span class="sxs-lookup"><span data-stu-id="3e14d-124">Call the [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) function to create a new **HSTRING**, and call the [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) function to release the reference to the backing string memory.</span></span> <span data-ttu-id="3e14d-125">Вызовите функцию [**виндовскреатестрингреференце**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , чтобы создать ссылку на строку, которая также называется *быстрой передачей строки*.</span><span class="sxs-lookup"><span data-stu-id="3e14d-125">Call the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function to create a string reference, which is also called a *fast-pass string*.</span></span>

<span data-ttu-id="3e14d-126">Скопируйте **HString** , вызвав функцию [**виндовсдупликатестринг**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .</span><span class="sxs-lookup"><span data-stu-id="3e14d-126">Copy an **HSTRING** by calling the [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) function.</span></span>

<span data-ttu-id="3e14d-127">Объедините две строки, вызвав функцию [**виндовсконкатстринг**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .</span><span class="sxs-lookup"><span data-stu-id="3e14d-127">Concatenate two strings by calling the [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) function.</span></span>

<span data-ttu-id="3e14d-128">Получите доступ к резервной памяти строки, вызвав функцию [**виндовсжетстрингравбуффер**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .</span><span class="sxs-lookup"><span data-stu-id="3e14d-128">Access the backing string memory by calling the [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) function.</span></span>

<span data-ttu-id="3e14d-129">**HString** может хранить и использовать внедренные символы **NUL** .</span><span class="sxs-lookup"><span data-stu-id="3e14d-129">**HSTRING** can store and use embedded **NUL** characters.</span></span> <span data-ttu-id="3e14d-130">Используйте функцию [**виндовсстрингхасембеддеднулл**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) для проверки внедренных символов **NUL** перед использованием любых функций, которые могут привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="3e14d-130">Use the [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) function to check for embedded **NUL** characters before using any functions which may produce unexpected results.</span></span> <span data-ttu-id="3e14d-131">Например, большинство функций Windows используют **лпквстр** в качестве входного параметра и вычисляют длину строки только до тех пор, пока не встретится первое значение **NUL** .</span><span class="sxs-lookup"><span data-stu-id="3e14d-131">For example, most of the Windows functions use **LPCWSTR** as an input parameter, and they compute the length of the string only until the first **NUL** is encountered.</span></span>

<span data-ttu-id="3e14d-132">Резервная строка должна оставаться неизменной и завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="3e14d-132">The backing string must remain immutable and null-terminated.</span></span> <span data-ttu-id="3e14d-133">При вызове кода создает ссылку на строку с помощью функции [**виндовскреатестрингреференце**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , память, которая содержит представление резервной строки, принадлежит вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="3e14d-133">When calling code creates a string reference by using the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function, the memory containing the backing string representation is owned by the caller.</span></span> <span data-ttu-id="3e14d-134">Среда выполнения Windows полагается на содержимое исходной строки, чтобы остаться без изменений.</span><span class="sxs-lookup"><span data-stu-id="3e14d-134">The Windows Runtime relies on the contents of the original string to remain unchanged.</span></span> <span data-ttu-id="3e14d-135">При передаче ссылки на строку в среда выполнения Windows, вызывающий объект следит за тем, чтобы содержимое строки было неизменным, а **NUL** была прервана на время вызова.</span><span class="sxs-lookup"><span data-stu-id="3e14d-135">When passing a string reference into the Windows Runtime, it is the caller’s responsibility to ensure that the string’s contents are unchanging and **NUL** terminated for the duration of the call.</span></span> <span data-ttu-id="3e14d-136">Среда выполнения Windows освобождает все ссылки на ссылку на строку, когда вызов возвращает.</span><span class="sxs-lookup"><span data-stu-id="3e14d-136">The Windows Runtime releases all references to the string reference when the call returns.</span></span>

<span data-ttu-id="3e14d-137">При получении **HString** в качестве выходного параметра рекомендуется присвоить этому обработчику **значение NULL** по завершении работы с ним.</span><span class="sxs-lookup"><span data-stu-id="3e14d-137">When you receive an **HSTRING** as an out parameter, it is good practice to set the handle to **NULL** when you are finished with it.</span></span>

<span data-ttu-id="3e14d-138">Вызовите функцию [**виндовспреаллокатестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) , чтобы выделить изменяемый буфер строк, который можно использовать для создания неизменяемого **HString**.</span><span class="sxs-lookup"><span data-stu-id="3e14d-138">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to allocate a mutable string buffer that you can use to create an immutable **HSTRING**.</span></span> <span data-ttu-id="3e14d-139">Завершив заполнение буфера, вызовите функцию [**виндовспромотестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) , чтобы создать **HString**.</span><span class="sxs-lookup"><span data-stu-id="3e14d-139">When you have finished populating the buffer, you call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) function to create the **HSTRING**.</span></span> <span data-ttu-id="3e14d-140">Этот шаблон двухстраничного конструкции позволяет реализовать функции, аналогичные "построителю строк".</span><span class="sxs-lookup"><span data-stu-id="3e14d-140">This two-phase construction pattern enables functionality that is similar to a "string builder."</span></span>

## <a name="requirements"></a><span data-ttu-id="3e14d-141">Требования</span><span class="sxs-lookup"><span data-stu-id="3e14d-141">Requirements</span></span>



| <span data-ttu-id="3e14d-142">Требование</span><span class="sxs-lookup"><span data-stu-id="3e14d-142">Requirement</span></span> | <span data-ttu-id="3e14d-143">Значение</span><span class="sxs-lookup"><span data-stu-id="3e14d-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e14d-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e14d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3e14d-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3e14d-145">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="3e14d-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e14d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3e14d-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e14d-147">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="3e14d-148">Header</span><span class="sxs-lookup"><span data-stu-id="3e14d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e14d-149"><dt>HString. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e14d-149"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e14d-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e14d-150">See also</span></span>

<dl> <span data-ttu-id="3e14d-151"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3e14d-151"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="3e14d-152">**виндовскреатестринг**</span><span class="sxs-lookup"><span data-stu-id="3e14d-152">**WindowsCreateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[<span data-ttu-id="3e14d-153">**виндовсделетестринг**</span><span class="sxs-lookup"><span data-stu-id="3e14d-153">**WindowsDeleteString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[<span data-ttu-id="3e14d-154">**виндовсдупликатестринг**</span><span class="sxs-lookup"><span data-stu-id="3e14d-154">**WindowsDuplicateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[<span data-ttu-id="3e14d-155">**виндовспреаллокатестрингбуффер**</span><span class="sxs-lookup"><span data-stu-id="3e14d-155">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
