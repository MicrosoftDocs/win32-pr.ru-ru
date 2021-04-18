---
description: Содержит текущее состояние создания сигнала для ПИН-кода.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: Структура PWM_PIN_IS_STARTED_OUTPUT (широт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655666"
---
# <a name="pwm_pin_is_started_output-structure"></a><span data-ttu-id="41862-103">Закрепление ШИРОТного \_ закрепления \_ \_ начинает \_ выходную структуру</span><span class="sxs-lookup"><span data-stu-id="41862-103">PWM\_PIN\_IS\_STARTED\_OUTPUT structure</span></span>

<span data-ttu-id="41862-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="41862-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="41862-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="41862-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="41862-106">Содержит текущее состояние создания сигнала для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="41862-106">Contains the current signal generation state of a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="41862-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41862-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="41862-108">Члены</span><span class="sxs-lookup"><span data-stu-id="41862-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="41862-109">**С начала**</span><span class="sxs-lookup"><span data-stu-id="41862-109">**IsStarted**</span></span>
</dt> <dd>

<span data-ttu-id="41862-110">Закрепление текущего состояния создания сигнала.</span><span class="sxs-lookup"><span data-stu-id="41862-110">The pin current signal generation state.</span></span> <span data-ttu-id="41862-111">Значение true означает, что ПИН-код запущен.</span><span class="sxs-lookup"><span data-stu-id="41862-111">A value of true means that the pin is started.</span></span> <span data-ttu-id="41862-112">Значение false означает, что ПИН-код остановлен.</span><span class="sxs-lookup"><span data-stu-id="41862-112">A value of false means that the pin is stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41862-113">Требования</span><span class="sxs-lookup"><span data-stu-id="41862-113">Requirements</span></span>



| <span data-ttu-id="41862-114">Требование</span><span class="sxs-lookup"><span data-stu-id="41862-114">Requirement</span></span> | <span data-ttu-id="41862-115">Значение</span><span class="sxs-lookup"><span data-stu-id="41862-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41862-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41862-116">Minimum supported client</span></span><br/> | <span data-ttu-id="41862-117">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="41862-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="41862-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41862-118">Minimum supported server</span></span><br/> | <span data-ttu-id="41862-119">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="41862-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="41862-120">Минимальная версия КМДФ</span><span class="sxs-lookup"><span data-stu-id="41862-120">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="41862-121">1,19</span><span class="sxs-lookup"><span data-stu-id="41862-121">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="41862-122">Минимальная версия UMDF</span><span class="sxs-lookup"><span data-stu-id="41862-122">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="41862-123">2.19</span><span class="sxs-lookup"><span data-stu-id="41862-123">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="41862-124">Header</span><span class="sxs-lookup"><span data-stu-id="41862-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="41862-125"><dt>Широт. h (включая широту. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41862-125"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41862-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41862-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41862-127">**\_ПИН-код модуляторного запроса IOCTL \_ \_ \_ запущен**</span><span class="sxs-lookup"><span data-stu-id="41862-127">**IOCTL\_PWM\_PIN\_IS\_STARTED**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




