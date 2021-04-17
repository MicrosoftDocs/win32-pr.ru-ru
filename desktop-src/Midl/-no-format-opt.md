---
title: no_format_opt Switch
description: Параметр/но в \_ формате \_ OPT изменяет способ оптимизации MIDL для типов и дескрипторов процедур.
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /no_format_opt параметр MIDL
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d6e54b963c9637c4f5a583fc9d8f44a0f2880e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681564"
---
# <a name="no_format_opt-switch"></a><span data-ttu-id="e20c5-104">/но \_ Формат \_ неявного переключения</span><span class="sxs-lookup"><span data-stu-id="e20c5-104">/no\_format\_opt switch</span></span>

<span data-ttu-id="e20c5-105">Параметр **/но в \_ формате \_ OPT** изменяет способ оптимизации MIDL для типов и дескрипторов процедур.</span><span class="sxs-lookup"><span data-stu-id="e20c5-105">The **/no\_format\_opt** switch changes the way MIDL optimizes type and procedure descriptors.</span></span>

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a><span data-ttu-id="e20c5-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="e20c5-106">Switch Options</span></span>

<span data-ttu-id="e20c5-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e20c5-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e20c5-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e20c5-108">Remarks</span></span>

<span data-ttu-id="e20c5-109">По умолчанию MIDL устраняет дублирование дескрипторов типа и процедур, чтобы уменьшить размер созданного кода-заглушки.</span><span class="sxs-lookup"><span data-stu-id="e20c5-109">By default, MIDL eliminates duplicate type and procedure descriptors in order to reduce the size of the generated stub code.</span></span> <span data-ttu-id="e20c5-110">Использование параметра **/но \_ формата " \_ неявное** " отключает это поведение оптимизации.</span><span class="sxs-lookup"><span data-stu-id="e20c5-110">Using the **/no\_format\_opt** switch turns off this optimizing behavior.</span></span>

## <a name="examples"></a><span data-ttu-id="e20c5-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="e20c5-111">Examples</span></span>

<span data-ttu-id="e20c5-112">**MIDL/но \_ Format \_ немилеан. idl**</span><span class="sxs-lookup"><span data-stu-id="e20c5-112">**midl /no\_format\_opt mylean.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="e20c5-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e20c5-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20c5-114">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="e20c5-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e20c5-115">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="e20c5-115">**/Oi**</span></span>](-oi.md)
</dt> </dl>

 

 




