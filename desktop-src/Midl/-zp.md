---
title: /ZP, параметр
description: Параметр/ZP совпадает с вариантом/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- MIDL/ZP Switch
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783696"
---
# <a name="zp-switch"></a><span data-ttu-id="e4be9-104">/ZP, параметр</span><span class="sxs-lookup"><span data-stu-id="e4be9-104">/Zp switch</span></span>

<span data-ttu-id="e4be9-105">Параметр **/Zp** совпадает с вариантом [**/Pack**](-pack.md) .</span><span class="sxs-lookup"><span data-stu-id="e4be9-105">The **/Zp** switch is the same as the [**/pack**](-pack.md) option.</span></span>

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a><span data-ttu-id="e4be9-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="e4be9-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="e4be9-107">*\_уровень упаковки*</span><span class="sxs-lookup"><span data-stu-id="e4be9-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="e4be9-108">Задает уровень упаковки для структур в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="e4be9-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="e4be9-109">Значение уровня упаковки может быть равно 1, 2, 4 или 8.</span><span class="sxs-lookup"><span data-stu-id="e4be9-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4be9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4be9-110">Remarks</span></span>

<span data-ttu-id="e4be9-111">Параметр **/Zp** обозначает уровень упаковки для структур в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="e4be9-111">The **/Zp** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="e4be9-112">Значение уровня упаковки соответствует значению параметра **/Zp** , используемому компилятором Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="e4be9-112">The packing-level value corresponds to the **/Zp** option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="e4be9-113">Дополнительные сведения см. в документации по программированию для Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="e4be9-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="e4be9-114">Укажите тот же уровень упаковки при вызове компилятора MIDL и компилятора C.</span><span class="sxs-lookup"><span data-stu-id="e4be9-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="e4be9-115">Уровень упаковки по умолчанию, используемый, если ни параметр **/Zp** , ни [**/Pack**](-pack.md) не указаны во всех средах сборки 8.</span><span class="sxs-lookup"><span data-stu-id="e4be9-115">The default packing level used when neither the **/Zp** nor [**/pack**](-pack.md) switch is specified is 8 in all build environments.</span></span>

> [!Note]  
> <span data-ttu-id="e4be9-116">Не используйте **/Zp1** или **/Zp2** на платформах MIPS или Alpha и не используйте **/Zp4** или **/Zp8** на 16-разрядных платформах.</span><span class="sxs-lookup"><span data-stu-id="e4be9-116">Do not use **/Zp1** or **/Zp2** on MIPS or Alpha platforms and do not use **/Zp4** or **/Zp8** on 16-bit platforms.</span></span> <span data-ttu-id="e4be9-117">В зависимости от типа данных и расположения памяти, назначенного компилятором C во время выполнения, это может привести к возникновению исключения неправильного выравнивания данных на платформах MIPS и Alpha.</span><span class="sxs-lookup"><span data-stu-id="e4be9-117">Depending on the data type and memory location assigned by the C compiler at run time, this can result in a data misalignment exception on MIPS and Alpha platforms.</span></span> <span data-ttu-id="e4be9-118">На платформах MS-DOS компилятор C не обеспечивает выравнивание по 4 или 8, поэтому приложение может завершить работу.</span><span class="sxs-lookup"><span data-stu-id="e4be9-118">On MS-DOS platforms, the C compiler will not ensure the alignment at 4 or 8, and so the application may terminate.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e4be9-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="e4be9-119">Examples</span></span>

<span data-ttu-id="e4be9-120">**MIDL/Zp4 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="e4be9-120">**midl /Zp4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="e4be9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4be9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4be9-122">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="e4be9-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e4be9-123">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="e4be9-123">**/pack**</span></span>](-pack.md)
</dt> </dl>

 

 




