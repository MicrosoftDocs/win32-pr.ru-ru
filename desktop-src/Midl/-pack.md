---
title: /Pack, параметр
description: Параметр/Pack совпадает с вариантом/Zp.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- MIDL/Pack Switch
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069120"
---
# <a name="pack-switch"></a><span data-ttu-id="f775f-104">/Pack, параметр</span><span class="sxs-lookup"><span data-stu-id="f775f-104">/pack switch</span></span>

<span data-ttu-id="f775f-105">Параметр **/Pack** совпадает с вариантом [**/Zp**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="f775f-105">The **/pack** switch is the same as the [**/Zp**](-zp.md) option.</span></span>

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a><span data-ttu-id="f775f-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="f775f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="f775f-107">*\_уровень упаковки*</span><span class="sxs-lookup"><span data-stu-id="f775f-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="f775f-108">Задает уровень упаковки для структур в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="f775f-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="f775f-109">Значение уровня упаковки может быть равно 1, 2, 4 или 8.</span><span class="sxs-lookup"><span data-stu-id="f775f-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f775f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f775f-110">Remarks</span></span>

<span data-ttu-id="f775f-111">Параметр **/Pack** обозначает уровень упаковки для структур в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="f775f-111">The **/pack** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="f775f-112">Значение уровня упаковки соответствует значению параметра [**/Zp**](-zp.md) , используемому компилятором Microsoft C/C++ версии 7,0.</span><span class="sxs-lookup"><span data-stu-id="f775f-112">The packing-level value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ version 7.0 compiler.</span></span> <span data-ttu-id="f775f-113">Дополнительные сведения см. в документации по программированию для Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="f775f-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="f775f-114">Укажите тот же уровень упаковки при вызове компилятора MIDL и компилятора C.</span><span class="sxs-lookup"><span data-stu-id="f775f-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span> <span data-ttu-id="f775f-115">Уровень упаковки по умолчанию, используемый, если ни параметр [**/Zp**](-zp.md) , ни **/Pack** не задан как 8 в обеих средах сборки.</span><span class="sxs-lookup"><span data-stu-id="f775f-115">The default packing level used when neither the [**/Zp**](-zp.md) nor **/pack** switch is specified is 8, in both all build environments.</span></span>

<span data-ttu-id="f775f-116">Обсуждение потенциальных опасностей при использовании нестандартных уровней упаковки см. в разделе справки [**/Zp**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="f775f-116">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="f775f-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="f775f-117">Examples</span></span>

<span data-ttu-id="f775f-118">**MIDL/Pack 2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="f775f-118">**midl /pack 2 filename.idl**</span></span>

<span data-ttu-id="f775f-119">**MIDL/Pack 8 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="f775f-119">**midl /pack 8 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f775f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f775f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f775f-121">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="f775f-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f775f-122">**/env**</span><span class="sxs-lookup"><span data-stu-id="f775f-122">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="f775f-123">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="f775f-123">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




