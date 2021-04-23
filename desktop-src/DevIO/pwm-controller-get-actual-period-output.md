---
description: Содержит действующий период вывода сигнала для контроллера ШИРОТы импульсов.
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: Структура PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT (широт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807408"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a><span data-ttu-id="8b195-103">Контроллер ШИРОТы \_ \_ получения \_ фактической \_ \_ структуры выходных данных периода</span><span class="sxs-lookup"><span data-stu-id="8b195-103">PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT structure</span></span>

<span data-ttu-id="8b195-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8b195-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8b195-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8b195-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8b195-106">Содержит действующий период вывода сигнала для контроллера ШИРОТы импульсов.</span><span class="sxs-lookup"><span data-stu-id="8b195-106">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b195-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b195-107">Syntax</span></span>


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="8b195-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8b195-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b195-109">**актуалпериод**</span><span class="sxs-lookup"><span data-stu-id="8b195-109">**ActualPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="8b195-110">Эффективный период вывода сигналов, который будет измеряться в выходных каналах контроллера.</span><span class="sxs-lookup"><span data-stu-id="8b195-110">The effective output signal period as it would be measured on the output channels of the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b195-111">Требования</span><span class="sxs-lookup"><span data-stu-id="8b195-111">Requirements</span></span>



| <span data-ttu-id="8b195-112">Требование</span><span class="sxs-lookup"><span data-stu-id="8b195-112">Requirement</span></span> | <span data-ttu-id="8b195-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8b195-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b195-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b195-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8b195-115">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8b195-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8b195-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b195-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8b195-117">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8b195-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8b195-118">Минимальная версия КМДФ</span><span class="sxs-lookup"><span data-stu-id="8b195-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="8b195-119">1,19</span><span class="sxs-lookup"><span data-stu-id="8b195-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="8b195-120">Минимальная версия UMDF</span><span class="sxs-lookup"><span data-stu-id="8b195-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="8b195-121">2.19</span><span class="sxs-lookup"><span data-stu-id="8b195-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="8b195-122">Header</span><span class="sxs-lookup"><span data-stu-id="8b195-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b195-123"><dt>Широт. h (включая широту. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b195-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b195-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b195-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b195-125">**\_ \_ \_ \_ текущий период получения контроллера ШИРОТного модулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="8b195-125">**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




