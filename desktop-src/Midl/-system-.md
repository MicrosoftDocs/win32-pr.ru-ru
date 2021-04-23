---
title: /системный коммутатор
description: Параметр/System указывает компилятору MIDL создать библиотеку типов для указанной системы. По умолчанию используется текущая операционная система.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /системный коммутатор MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334168"
---
# <a name="system-switch"></a><span data-ttu-id="f38da-105">/<system> ключом</span><span class="sxs-lookup"><span data-stu-id="f38da-105">/<system> switch</span></span>

<span data-ttu-id="f38da-106">**/<system>** Параметр указывает компилятору MIDL создать библиотеку типов для указанной системы.</span><span class="sxs-lookup"><span data-stu-id="f38da-106">The **/<system>** switch directs the MIDL compiler to generate a type library for the specified system.</span></span> <span data-ttu-id="f38da-107">По умолчанию используется текущая операционная система.</span><span class="sxs-lookup"><span data-stu-id="f38da-107">The default is the current operating system.</span></span>

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a><span data-ttu-id="f38da-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="f38da-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="f38da-109"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f38da-109"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="f38da-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f38da-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="f38da-111"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f38da-111"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="f38da-112">64-разрядная среда Windows на базе Intel, например Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f38da-112">An Intel-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="f38da-113"><span id="amd64"></span><span id="AMD64"></span>AMD64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f38da-113"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="f38da-114">64-разрядная среда Windows на базе американской микроустройств, например Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f38da-114">An American Micro Devices-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f38da-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f38da-115">Remarks</span></span>

<span data-ttu-id="f38da-116">Этот параметр **/<system>** функционально аналогичен параметру MIDL [**/env**](-env.md) и распознается компилятором MIDL исключительно для обеспечения обратной совместимости с MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="f38da-116">The **/<system>** switch is functionally the same as the MIDL [**/env**](-env.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span> <span data-ttu-id="f38da-117">При создании нового файла makefile используйте параметр **/env** .</span><span class="sxs-lookup"><span data-stu-id="f38da-117">If you are generating a new makefile, use the **/env** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="f38da-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="f38da-118">Examples</span></span>

<span data-ttu-id="f38da-119">**MIDL/Win32 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="f38da-119">**midl /win32 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f38da-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f38da-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38da-121">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="f38da-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f38da-122">**/env**</span><span class="sxs-lookup"><span data-stu-id="f38da-122">**/env**</span></span>](-env.md)
</dt> </dl>

 

 




