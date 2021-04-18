---
description: Следующие флаги задают уровень динамического повторного подключения, который будет использоваться во время подготовки к просмотру.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Динамические флаги повторного подключения (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675335"
---
# <a name="dynamic-reconnection-flags"></a><span data-ttu-id="253ce-103">Динамические флаги повторного подключения</span><span class="sxs-lookup"><span data-stu-id="253ce-103">Dynamic Reconnection Flags</span></span>

<span data-ttu-id="253ce-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="253ce-104">\[Deprecated.</span></span> <span data-ttu-id="253ce-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="253ce-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="253ce-106">Следующие флаги задают уровень динамического повторного подключения, который будет использоваться во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="253ce-106">The following flags specify the level of dynamic reconnection to use during rendering.</span></span>



| <span data-ttu-id="253ce-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="253ce-107">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="253ce-108">Описание</span><span class="sxs-lookup"><span data-stu-id="253ce-108">Description</span></span>                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <span data-ttu-id="253ce-109"><dt>**Коннектф \_ ДИНАМИЧЕСКИЙ \_ нет**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="253ce-109"><dt>**CONNECTF\_DYNAMIC\_NONE**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="253ce-110">Динамическое повторное подключение отсутствует.</span><span class="sxs-lookup"><span data-stu-id="253ce-110">No dynamic reconnection.</span></span> <span data-ttu-id="253ce-111">Загрузите все перед отрисовкой проекта.</span><span class="sxs-lookup"><span data-stu-id="253ce-111">Load everything before rendering the project.</span></span><br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <span data-ttu-id="253ce-112"><dt>**Коннектф \_ ДИНАМИЧЕСКИЕ \_ источники**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="253ce-112"><dt>**CONNECTF\_DYNAMIC\_SOURCES**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="253ce-113">Загружать источники только по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="253ce-113">Load sources only as needed.</span></span><br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <span data-ttu-id="253ce-114"><dt>**Коннектф \_ ДИНАМИЧЕСКИЕ \_ эффекты**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="253ce-114"><dt>**CONNECTF\_DYNAMIC\_EFFECTS**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="253ce-115">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="253ce-115">Reserved.</span></span> <span data-ttu-id="253ce-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="253ce-116">Do not use.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="253ce-117">Требования</span><span class="sxs-lookup"><span data-stu-id="253ce-117">Requirements</span></span>



| <span data-ttu-id="253ce-118">Требование</span><span class="sxs-lookup"><span data-stu-id="253ce-118">Requirement</span></span> | <span data-ttu-id="253ce-119">Значение</span><span class="sxs-lookup"><span data-stu-id="253ce-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="253ce-120">Header</span><span class="sxs-lookup"><span data-stu-id="253ce-120">Header</span></span><br/> | <dl> <span data-ttu-id="253ce-121"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="253ce-121"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="253ce-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="253ce-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253ce-123">**Ирендеренгине:: Сетдинамикреконнектлевел**</span><span class="sxs-lookup"><span data-stu-id="253ce-123">**IRenderEngine::SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




