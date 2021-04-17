---
title: /env, параметр
description: Параметр/env выбирает среду, в которой выполняется приложение.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- MIDL/env Switch
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412830"
---
# <a name="env-switch"></a><span data-ttu-id="4714c-104">/env, параметр</span><span class="sxs-lookup"><span data-stu-id="4714c-104">/env switch</span></span>

<span data-ttu-id="4714c-105">Параметр **/env** выбирает среду, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="4714c-105">The **/env** switch selects the environment in which the application runs.</span></span>

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a><span data-ttu-id="4714c-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="4714c-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="4714c-107"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4714c-107"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4714c-108">Направляет компилятор MIDL для создания файлов заглушек или файла библиотеки типов для 32-разрядной среды.</span><span class="sxs-lookup"><span data-stu-id="4714c-108">Directs the MIDL compiler to generate stub files, or a type library file, for a 32-bit environment.</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="4714c-109"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4714c-109"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4714c-110">Направляет компилятор MIDL для создания файлов заглушек или файла библиотеки типов для среды архитектуры Intel 64-bit (IA64).</span><span class="sxs-lookup"><span data-stu-id="4714c-110">Directs the MIDL compiler to generate stub files, or a type library file, for a Intel Architecture 64-bit (IA64) environment.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="4714c-111"><span id="amd64"></span><span id="AMD64"></span>AMD64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4714c-111"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4714c-112">Направляет компилятор MIDL для создания файлов заглушек или файла библиотеки типов для среды с расширенными микроустройствами 64-бит (AMD64).</span><span class="sxs-lookup"><span data-stu-id="4714c-112">Directs the MIDL compiler to generate stub files, or a type library file, for an Advanced Micro Devices 64-bit (AMD64) environment.</span></span>

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span data-ttu-id="4714c-113"><span id="win64"></span><span id="WIN64"></span>Win64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4714c-113"><span id="win64"></span><span id="WIN64"></span>\*\*\*\*win64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4714c-114">Такое же поведение, что и для *ia64*.</span><span class="sxs-lookup"><span data-stu-id="4714c-114">Same behavior as *ia64*.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4714c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4714c-115">Remarks</span></span>

<span data-ttu-id="4714c-116">Параметр **/env** в основном влияет на уровень упаковки, используемый для структур в этой среде.</span><span class="sxs-lookup"><span data-stu-id="4714c-116">The **/env** switch primarily affects the packing level used for structures in that environment.</span></span> <span data-ttu-id="4714c-117">Убедитесь, что задан один и тот же параметр уровня упаковки для компилятора MIDL и компилятора C.</span><span class="sxs-lookup"><span data-stu-id="4714c-117">Be sure you specify the same packing-level setting for both the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="4714c-118">Параметр **/env** определяет уровень упаковки и другие параметры следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4714c-118">The **/env** switch determines the packing level and other settings as follows:</span></span>

-   <span data-ttu-id="4714c-119">При указании **Win32** созданные заглушки используют для всех типов, участвующих в удаленных операциях, уровень упаковки C-компилятора 8.</span><span class="sxs-lookup"><span data-stu-id="4714c-119">When you specify **win32**, generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="4714c-120">Типы данных [**int**](int.md) — 32 бит.</span><span class="sxs-lookup"><span data-stu-id="4714c-120">The [**int**](int.md) data types are both 32 bits.</span></span> <span data-ttu-id="4714c-121">Указатели — это 32 бит.</span><span class="sxs-lookup"><span data-stu-id="4714c-121">Pointers are 32 bits.</span></span>
-   <span data-ttu-id="4714c-122">При указании **ia64** или **AMD64** компилятор MIDL выполняется в режиме кросс-компилятора для указанной (Intel или AMD) 64-разрядной платформы.</span><span class="sxs-lookup"><span data-stu-id="4714c-122">When you specify **ia64** or **amd64**, the MIDL compiler runs in a cross-compiler mode for the indicated (Intel or AMD) 64-bit platform.</span></span> <span data-ttu-id="4714c-123">Созданные заглушки используют для всех типов, участвующих в удаленных операциях, уровень упаковки C-компилятора 8.</span><span class="sxs-lookup"><span data-stu-id="4714c-123">The generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="4714c-124">Типы данных [**Long**](long.md) и [**int**](int.md) — 32 бит.</span><span class="sxs-lookup"><span data-stu-id="4714c-124">The [**long**](long.md) and [**int**](int.md) data types are 32 bits.</span></span> <span data-ttu-id="4714c-125">Указатели — это 64 бит.</span><span class="sxs-lookup"><span data-stu-id="4714c-125">Pointers are 64 bits.</span></span>

<span data-ttu-id="4714c-126">Параметры [**/align**](-align.md), [**/Pack**](-pack.md)и [**/Zp**](-zp.md) имеют приоритет над параметрами **/env** .</span><span class="sxs-lookup"><span data-stu-id="4714c-126">The [**/align**](-align.md), [**/pack**](-pack.md), and [**/Zp**](-zp.md) switches take precedence over the **/env** settings.</span></span>

<span data-ttu-id="4714c-127">Дополнительные сведения о 64-разрядной поддержке MIDL и RPC см. в статье [Разработка интерфейсов, совместимых с 64](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span><span class="sxs-lookup"><span data-stu-id="4714c-127">For more information on 64 bit support for MIDL and RPC see [Designing 64-bit-Compatible Interfaces](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span></span>

## <a name="examples"></a><span data-ttu-id="4714c-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="4714c-128">Examples</span></span>

<span data-ttu-id="4714c-129">**MIDL/env Win32 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="4714c-129">**midl /env win32 filename.idl**</span></span>

<span data-ttu-id="4714c-130">**MIDL/env ia64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="4714c-130">**midl /env ia64 filename.idl**</span></span>

<span data-ttu-id="4714c-131">**MIDL/env AMD64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="4714c-131">**midl /env amd64 filename.idl**</span></span>

<span data-ttu-id="4714c-132">**MIDL/env Win64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="4714c-132">**midl /env win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="4714c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4714c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4714c-134">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="4714c-134">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="4714c-135">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="4714c-135">**/pack**</span></span>](-pack.md)
</dt> <dt>

[<span data-ttu-id="4714c-136">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="4714c-136">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 