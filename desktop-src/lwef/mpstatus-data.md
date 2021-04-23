---
title: Структура MPSTATUS_DATA (Мпклиент. h)
description: Содержит данные о текущем состоянии компонента продукта.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA структуры устаревшие функции среды Windows
- Функции PMPSTATUS_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802878"
---
# <a name="mpstatus_data-structure"></a><span data-ttu-id="ef5e3-105">\_Структура данных мпстатус</span><span class="sxs-lookup"><span data-stu-id="ef5e3-105">MPSTATUS\_DATA structure</span></span>

<span data-ttu-id="ef5e3-106">Содержит данные о текущем состоянии компонента продукта.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-106">Contains data about the current status of a component of the product.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef5e3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef5e3-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a><span data-ttu-id="ef5e3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ef5e3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef5e3-109">**ComponentID**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-109">**ComponentID**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-110">Тип: **[ **мпкомпонент \_ ID**](mpcomponent-id.md)**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-110">Type: **[**MPCOMPONENT\_ID**](mpcomponent-id.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-111">Конкретный идентификатор компонента, для которого сообщается состояние.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-111">Specific component ID for which status is reported.</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-112">**фенабле**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-112">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-113">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="ef5e3-113">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-114">Состояние, запрошенное для компонента.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-114">Status requested for the component.</span></span> <span data-ttu-id="ef5e3-115">**hResult** в данных обратного вызова обозначает успешность или неудачу запроса.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-115">**hResult** in the callback data signifies success or failure for the request.</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-116">**компонентстатус**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-116">**ComponentStatus**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-117">Дополнительные данные о состоянии в зависимости от значения **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-117">Extra status data depending on value of **ComponentID**.</span></span>

> [!Note]  
> <span data-ttu-id="ef5e3-118">В настоящее время приводится указатель на фиктивную структуру для всех возможных значений **компонента ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-118">Currently results in a pointer to a dummy structure for all possible values of **ComponentID**.</span></span>

 

<dl> <dt>

<span data-ttu-id="ef5e3-119">**ниже**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-119">**p1**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-120">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-120">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-121">Когда **ComponentID**  ==  **мпкомпонент \_ в качестве \_ сигнатуры**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-121">When **ComponentID** == **MPCOMPONENT\_AS\_SIGNATURE**.</span></span> <span data-ttu-id="ef5e3-122">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-122">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-123">**–**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-123">**p2**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-124">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-124">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-125">При   ==  **\_ \_ сигнатуре ComponentID мпкомпонент AV**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-125">When **ComponentID** == **MPCOMPONENT\_AV\_SIGNATURE**.</span></span> <span data-ttu-id="ef5e3-126">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-126">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-127">**–**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-127">**p3**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-128">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-128">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-129">При   ==  **\_ \_ мониторе ComponentID мпкомпонент в режиме реального времени**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-129">When **ComponentID** == **MPCOMPONENT\_REALTIME\_MONITOR**.</span></span> <span data-ttu-id="ef5e3-130">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-130">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-131">**P4**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-131">**p4**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-132">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-132">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-133">Когда **ComponentID**  ==  **мпкомпонент \_ \_ защиты доступа**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-133">When **ComponentID** == **MPCOMPONENT\_ONACCESS\_PROTECTION**.</span></span> <span data-ttu-id="ef5e3-134">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-134">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-135">**P5**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-135">**p5**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-136">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-136">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-137">Когда **ComponentID**  ==  **мпкомпонент \_ защиту ioav \_ Protection**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-137">When **ComponentID** == **MPCOMPONENT\_IOAV\_PROTECTION**.</span></span> <span data-ttu-id="ef5e3-138">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-138">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-139">**архитектур**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-139">**p6**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-140">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-140">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-141">При   ==  **\_ \_ мониторе поведения ComponentID мпкомпонент**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-141">When **ComponentID** == **MPCOMPONENT\_BEHAVIOR\_MONITOR**.</span></span> <span data-ttu-id="ef5e3-142">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-142">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-143">**P7**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-143">**p7**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-144">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-144">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-145">При   ==  **\_ автоматическом \_ сканировании ComponentID мпкомпонент**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-145">When **ComponentID** == **MPCOMPONENT\_AUTO\_SCAN**.</span></span> <span data-ttu-id="ef5e3-146">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-146">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-147">**P8**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-147">**p8**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-148">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-148">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-149">Когда **ComponentID**  ==  **мпкомпонент \_ Auto \_ сигупдате**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-149">When **ComponentID** == **MPCOMPONENT\_AUTO\_SIGUPDATE**.</span></span> <span data-ttu-id="ef5e3-150">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-150">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-151">**P9**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-151">**p9**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-152">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-152">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-153">Когда **ComponentID**  ==  **мпкомпонент \_ IPC**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-153">When **ComponentID** == **MPCOMPONENT\_IPC**.</span></span> <span data-ttu-id="ef5e3-154">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-154">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-155">**pa**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-155">**pa**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-156">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-156">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-157">Когда **ComponentID**  ==  **мпкомпонент \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-157">When **ComponentID** == **MPCOMPONENT\_NIS**.</span></span> <span data-ttu-id="ef5e3-158">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-158">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef5e3-159">**МС**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-159">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="ef5e3-160">Тип: **пмпстатус \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-160">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ef5e3-161">Когда **ComponentID**  ==  **мпкомпонент \_ ELAM**.</span><span class="sxs-lookup"><span data-stu-id="ef5e3-161">When **ComponentID** == **MPCOMPONENT\_ELAM**.</span></span> <span data-ttu-id="ef5e3-162">См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ef5e3-162">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef5e3-163">Требования</span><span class="sxs-lookup"><span data-stu-id="ef5e3-163">Requirements</span></span>



| <span data-ttu-id="ef5e3-164">Требование</span><span class="sxs-lookup"><span data-stu-id="ef5e3-164">Requirement</span></span> | <span data-ttu-id="ef5e3-165">Значение</span><span class="sxs-lookup"><span data-stu-id="ef5e3-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5e3-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef5e3-166">Minimum supported client</span></span><br/> | <span data-ttu-id="ef5e3-167">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef5e3-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ef5e3-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef5e3-168">Minimum supported server</span></span><br/> | <span data-ttu-id="ef5e3-169">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef5e3-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef5e3-170">Header</span><span class="sxs-lookup"><span data-stu-id="ef5e3-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef5e3-171"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef5e3-171"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef5e3-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef5e3-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef5e3-173">**\_идентификатор мпкомпонент**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-173">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="ef5e3-174">**МПСТАТУС \_ датаекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ef5e3-174">**MPSTATUS\_DATAEX\_UNUSED**</span></span>](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





