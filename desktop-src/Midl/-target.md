---
title: Ключ "/target"
description: Параметр/Target позволяет компилятору MIDL включить оптимизацию, доступную только в последних версиях Windows. Параметр/target автоматически активирует дополнительные параметры.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- Параметр/target MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104081660"
---
# <a name="target-switch"></a><span data-ttu-id="d85a6-105">Ключ "/target"</span><span class="sxs-lookup"><span data-stu-id="d85a6-105">/target switch</span></span>

<span data-ttu-id="d85a6-106">Параметр **/Target** позволяет компилятору MIDL включить оптимизацию, доступную только в последних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="d85a6-106">The **/target** switch enables the MIDL compiler to enable optimizations available only on recent versions of Windows.</span></span> <span data-ttu-id="d85a6-107">Параметр **/Target** автоматически активирует дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="d85a6-107">The **/target** switch automatically activates additional switches.</span></span>

``` syntax
midl /target level
```

## <a name="switch-options"></a><span data-ttu-id="d85a6-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="d85a6-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d85a6-109">*level*</span><span class="sxs-lookup"><span data-stu-id="d85a6-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="d85a6-110">Задает целевой уровень, например NT50, NT51, NT60, NT61, NT62 или NT100.</span><span class="sxs-lookup"><span data-stu-id="d85a6-110">Specifies the target level, such as NT50, NT51, NT60, NT61, NT62, or NT100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d85a6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d85a6-111">Remarks</span></span>

<span data-ttu-id="d85a6-112">Параметр **/Target** автоматически активирует дополнительные коммутаторы на основе операционной системы, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d85a6-112">The **/target** switch automatically activates additional switches, based on the operating system, as specified in the following table:</span></span>



| <span data-ttu-id="d85a6-113">Операционная система</span><span class="sxs-lookup"><span data-stu-id="d85a6-113">Operating system</span></span> | <span data-ttu-id="d85a6-114">уровень/Target</span><span class="sxs-lookup"><span data-stu-id="d85a6-114">/target level</span></span> | <span data-ttu-id="d85a6-115">Активированные переключатели</span><span class="sxs-lookup"><span data-stu-id="d85a6-115">Switches Activated</span></span>                     |
|------------------|---------------|----------------------------------------|
| <span data-ttu-id="d85a6-116">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d85a6-116">Windows 2000</span></span>     | <span data-ttu-id="d85a6-117">NT50</span><span class="sxs-lookup"><span data-stu-id="d85a6-117">NT50</span></span>          | <span data-ttu-id="d85a6-118">/Oicf/Error ALL/robust</span><span class="sxs-lookup"><span data-stu-id="d85a6-118">/Oicf /error all /robust</span></span>               |
| <span data-ttu-id="d85a6-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d85a6-119">Windows XP</span></span>       | <span data-ttu-id="d85a6-120">NT51</span><span class="sxs-lookup"><span data-stu-id="d85a6-120">NT51</span></span>          | <span data-ttu-id="d85a6-121">/Oicf/Error все/robust/протокол</span><span class="sxs-lookup"><span data-stu-id="d85a6-121">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="d85a6-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d85a6-122">Windows Vista</span></span>    | <span data-ttu-id="d85a6-123">NT60</span><span class="sxs-lookup"><span data-stu-id="d85a6-123">NT60</span></span>          | <span data-ttu-id="d85a6-124">/Oicf/Error все/robust/протокол</span><span class="sxs-lookup"><span data-stu-id="d85a6-124">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="d85a6-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d85a6-125">Windows 7</span></span>        | <span data-ttu-id="d85a6-126">NT61</span><span class="sxs-lookup"><span data-stu-id="d85a6-126">NT61</span></span>          | <span data-ttu-id="d85a6-127">/Oicf/Error все/robust/протокол</span><span class="sxs-lookup"><span data-stu-id="d85a6-127">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="d85a6-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d85a6-128">Windows 8</span></span>        | <span data-ttu-id="d85a6-129">NT62</span><span class="sxs-lookup"><span data-stu-id="d85a6-129">NT62</span></span>          | <span data-ttu-id="d85a6-130">/Oicf/Error все/robust/протокол</span><span class="sxs-lookup"><span data-stu-id="d85a6-130">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="d85a6-131">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d85a6-131">Windows 10</span></span>       | <span data-ttu-id="d85a6-132">NT100</span><span class="sxs-lookup"><span data-stu-id="d85a6-132">NT100</span></span>         | <span data-ttu-id="d85a6-133">/Oicf/Error все/robust/протокол</span><span class="sxs-lookup"><span data-stu-id="d85a6-133">/Oicf /error all /robust /protocol all</span></span> |
 

<span data-ttu-id="d85a6-134">Чтобы обеспечить выполнение заглушки в системе, заданной параметром **/Target** , MIDL выдает ошибку, если имеется функция, доступная только в более поздней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d85a6-134">To ensure a stub runs on the system specified by the **/target** switch, MIDL issues an error when a feature available only on a more recent version of Windows is present.</span></span> <span data-ttu-id="d85a6-135">В следующей таблице указан минимальный уровень **/Target** , необходимый для включения компонента.</span><span class="sxs-lookup"><span data-stu-id="d85a6-135">The following table specifies the minimum **/target** level required to enable the feature.</span></span> <span data-ttu-id="d85a6-136">Более высокие уровни целевого объекта включают все функции с более низким уровнем целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="d85a6-136">Higher target levels include all features from lower target levels.</span></span>



| <span data-ttu-id="d85a6-137">Минимальный требуемый уровень/Target</span><span class="sxs-lookup"><span data-stu-id="d85a6-137">Minimum required /target level</span></span> | <span data-ttu-id="d85a6-138">Компоненты</span><span class="sxs-lookup"><span data-stu-id="d85a6-138">Features</span></span>                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d85a6-139">NT50</span><span class="sxs-lookup"><span data-stu-id="d85a6-139">NT50</span></span>                           | <span data-ttu-id="d85a6-140">/robust</span><span class="sxs-lookup"><span data-stu-id="d85a6-140">/robust</span></span><br/> <span data-ttu-id="d85a6-141">\[message\]</span><span class="sxs-lookup"><span data-stu-id="d85a6-141">\[message\]</span></span><br/> <span data-ttu-id="d85a6-142">\[async\]</span><span class="sxs-lookup"><span data-stu-id="d85a6-142">\[async\]</span></span><br/> <span data-ttu-id="d85a6-143">\[асинхронный \_ UUID\]</span><span class="sxs-lookup"><span data-stu-id="d85a6-143">\[async\_uuid\]</span></span><br/> <span data-ttu-id="d85a6-144">\[уведомлять \] в режиме/Oicf</span><span class="sxs-lookup"><span data-stu-id="d85a6-144">\[notify\] in /Oicf mode</span></span><br/> <span data-ttu-id="d85a6-145">\[кодирование \] или \[ декодирование \] в режиме/Oicf</span><span class="sxs-lookup"><span data-stu-id="d85a6-145">\[encode\] or \[decode\] in /Oicf mode</span></span><br/>                   |
| <span data-ttu-id="d85a6-146">NT51</span><span class="sxs-lookup"><span data-stu-id="d85a6-146">NT51</span></span>                           | <span data-ttu-id="d85a6-147">поддержка/протокол 64-bit</span><span class="sxs-lookup"><span data-stu-id="d85a6-147">/protocol 64-bit support</span></span><br/> <span data-ttu-id="d85a6-148">\[частичный \_ пропуск\]</span><span class="sxs-lookup"><span data-stu-id="d85a6-148">\[partial\_ignore\]</span></span><br/> <span data-ttu-id="d85a6-149">\[принудительное \_ выделение\]</span><span class="sxs-lookup"><span data-stu-id="d85a6-149">\[force\_allocate\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="d85a6-150">NT60</span><span class="sxs-lookup"><span data-stu-id="d85a6-150">NT60</span></span>                           | <span data-ttu-id="d85a6-151">Маршалинг принудительной сложной структуры</span><span class="sxs-lookup"><span data-stu-id="d85a6-151">Forced complex structure marshalling</span></span><br/> <span data-ttu-id="d85a6-152">Дескрипторы контекста в массиве или структуре</span><span class="sxs-lookup"><span data-stu-id="d85a6-152">Context handles in an array or structure</span></span><br/> <span data-ttu-id="d85a6-153">\[\]Поддержка диапазона для неразмерных строк</span><span class="sxs-lookup"><span data-stu-id="d85a6-153">\[range\] support for unsized strings</span></span><br/> <span data-ttu-id="d85a6-154">\[Тип \_ строгого \_ \_ маркера контекста\]</span><span class="sxs-lookup"><span data-stu-id="d85a6-154">\[type\_strict\_context\_handle\]</span></span><br/> |
| <span data-ttu-id="d85a6-155">NT61</span><span class="sxs-lookup"><span data-stu-id="d85a6-155">NT61</span></span>                           | <span data-ttu-id="d85a6-156">Прямые вызовы заглушек COM для интерфейсов с менее чем 32 методами требуют связывания заглушек COM с **OLE32.DLL**.</span><span class="sxs-lookup"><span data-stu-id="d85a6-156">Direct COM stub calls for interfaces with less than 32 methods requires linking COM stubs with **OLE32.DLL**.</span></span><br/>                                                                          |
| <span data-ttu-id="d85a6-157">NT62</span><span class="sxs-lookup"><span data-stu-id="d85a6-157">NT62</span></span>                           | <span data-ttu-id="d85a6-158">Поддержка ARM</span><span class="sxs-lookup"><span data-stu-id="d85a6-158">ARM support</span></span><br/> <span data-ttu-id="d85a6-159">Поддержка WinRT</span><span class="sxs-lookup"><span data-stu-id="d85a6-159">WinRT support</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="d85a6-160">NT100</span><span class="sxs-lookup"><span data-stu-id="d85a6-160">NT100</span></span>                          | <span data-ttu-id="d85a6-161">\[\]поддержка system_handle</span><span class="sxs-lookup"><span data-stu-id="d85a6-161">\[system_handle\] support</span></span><br /> |


 

## <a name="examples"></a><span data-ttu-id="d85a6-162">Примеры</span><span class="sxs-lookup"><span data-stu-id="d85a6-162">Examples</span></span>

<span data-ttu-id="d85a6-163">**MIDL/Target NT50**</span><span class="sxs-lookup"><span data-stu-id="d85a6-163">**midl /target NT50**</span></span>

## <a name="see-also"></a><span data-ttu-id="d85a6-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d85a6-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d85a6-165">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="d85a6-165">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d85a6-166">**/осф**</span><span class="sxs-lookup"><span data-stu-id="d85a6-166">**/osf**</span></span>](-osf.md)
</dt> </dl>
