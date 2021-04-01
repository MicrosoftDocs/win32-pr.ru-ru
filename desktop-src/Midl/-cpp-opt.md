---
title: cpp_opt Switch
description: Параметр/КПП \_ OPT указывает параметры для передачи препроцессору C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt параметр MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104414280"
---
# <a name="cpp_opt-switch"></a><span data-ttu-id="a6ff6-104">/КПП \_ Неявное переключение</span><span class="sxs-lookup"><span data-stu-id="a6ff6-104">/cpp\_opt switch</span></span>

<span data-ttu-id="a6ff6-105">Параметр **/КПП \_ OPT** указывает параметры для передачи препроцессору C/C++.</span><span class="sxs-lookup"><span data-stu-id="a6ff6-105">The **/cpp\_opt** switch specifies options to pass to the C/C++ preprocessor.</span></span>

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a><span data-ttu-id="a6ff6-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="a6ff6-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="a6ff6-107">*\_Параметр препроцессора \_ C*</span><span class="sxs-lookup"><span data-stu-id="a6ff6-107">*C\_preprocessor\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ff6-108">Задает параметр командной строки, связанный с вызываемым препроцессором.</span><span class="sxs-lookup"><span data-stu-id="a6ff6-108">Specifies command-line option associated with the invoked preprocessor.</span></span> 

<span data-ttu-id="a6ff6-109">**Примечание**. для препроцессоров Microsoft C/C++ необходимо указать `/E` параметр в виде части строки *\_ \_ параметра препроцессора c* .</span><span class="sxs-lookup"><span data-stu-id="a6ff6-109">**Note**: For the Microsoft C/C++ preprocessors you must supply the `/E` switch as part of the *C\_preprocessor\_option* string.</span></span> 

<span data-ttu-id="a6ff6-110">Кавычки требуются, если используется более одного параметра и для пробелов.</span><span class="sxs-lookup"><span data-stu-id="a6ff6-110">Quotes are required when more than one option is used, and for spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6ff6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6ff6-111">Remarks</span></span>

<span data-ttu-id="a6ff6-112">Не используйте этот параметр, если нет конкретной причины для этого.</span><span class="sxs-lookup"><span data-stu-id="a6ff6-112">Do not use this switch unless there is a specific reason for doing so.</span></span> <span data-ttu-id="a6ff6-113">Дополнительные сведения о предварительной обработке см. [в документации C-требования к препроцессору для MIDL](c-preprocessor-requirements-for-midl.md) .</span><span class="sxs-lookup"><span data-stu-id="a6ff6-113">Consult [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for important information regarding preprocessing.</span></span>

<span data-ttu-id="a6ff6-114">Параметр **/КПП \_ OPT** можно использовать с параметром [**/КПП \_ cmd**](-cpp-cmd.md) или без него.</span><span class="sxs-lookup"><span data-stu-id="a6ff6-114">The **/cpp\_opt** switch can be used with or without the [**/cpp\_cmd**](-cpp-cmd.md) switch.</span></span> <span data-ttu-id="a6ff6-115">Дополнительные сведения о создании командной строки препроцессора в любом случае см. в **/КПП \_ cmd** .</span><span class="sxs-lookup"><span data-stu-id="a6ff6-115">Consult **/cpp\_cmd** for details of how the preprocessor command line is constructed in either case.</span></span>

<span data-ttu-id="a6ff6-116">Параметр **/КПП \_ OPT** , если он указан, должен всегда включать `/E` в себя для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="a6ff6-116">The **/cpp\_opt** switch, if specified, must always include `/E` in order to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="a6ff6-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="a6ff6-117">Examples</span></span>

<span data-ttu-id="a6ff6-118">**MIDL/КПП \_ cmd d: \\ NT \\ tools \\ ia64 \\cl.exe/дфлаг = true/ИК: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="a6ff6-118">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="a6ff6-119">**MIDL/КПП \_ cmd "микпп"/дфлаг = true/ИК: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="a6ff6-119">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="a6ff6-120">**MIDL/КПП \_ OPT "/E/дфлаг = true/ИК: \\ Inc" имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="a6ff6-120">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="a6ff6-121">**MIDL/КПП \_ cmd "CL"/КПП \_ OPT "/e/ДФЛАГ = true/ИК: \\ Inc" имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="a6ff6-121">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="a6ff6-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6ff6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ff6-123">**/савепп**</span><span class="sxs-lookup"><span data-stu-id="a6ff6-123">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="a6ff6-124">**/КПП \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="a6ff6-124">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="a6ff6-125">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="a6ff6-125">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a6ff6-126">**/но \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="a6ff6-126">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="a6ff6-127">Требования к препроцессору C-препроцессор для MIDL</span><span class="sxs-lookup"><span data-stu-id="a6ff6-127">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




