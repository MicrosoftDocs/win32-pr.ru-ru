---
description: Содержит требуемый процент циклов пошлины для ПИН-кода или канала в контроллере широты импульсов.
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Структура PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (широт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423202"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a><span data-ttu-id="4da55-103">Закрепление ШИРОТного \_ закрепления. \_ \_ \_ \_ \_ процент \_ входных данных цикла активной пошлины</span><span class="sxs-lookup"><span data-stu-id="4da55-103">PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT structure</span></span>

<span data-ttu-id="4da55-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4da55-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4da55-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4da55-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4da55-106">Содержит требуемый процент циклов пошлины для ПИН-кода или канала в контроллере широты импульсов.</span><span class="sxs-lookup"><span data-stu-id="4da55-106">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da55-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4da55-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a><span data-ttu-id="4da55-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4da55-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4da55-109">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="4da55-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="4da55-110">Требуемый цикл обработки сигнала ШИРОТы в виде коэффициента ШИРОТы в \_ процентах (улонглонг).</span><span class="sxs-lookup"><span data-stu-id="4da55-110">The desired PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4da55-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4da55-111">Requirements</span></span>



| <span data-ttu-id="4da55-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4da55-112">Requirement</span></span> | <span data-ttu-id="4da55-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4da55-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da55-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4da55-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4da55-115">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4da55-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4da55-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4da55-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4da55-117">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="4da55-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4da55-118">Минимальная версия КМДФ</span><span class="sxs-lookup"><span data-stu-id="4da55-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="4da55-119">1,19</span><span class="sxs-lookup"><span data-stu-id="4da55-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="4da55-120">Минимальная версия UMDF</span><span class="sxs-lookup"><span data-stu-id="4da55-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="4da55-121">2.19</span><span class="sxs-lookup"><span data-stu-id="4da55-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="4da55-122">Header</span><span class="sxs-lookup"><span data-stu-id="4da55-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da55-123"><dt>Широт. h (включая широту. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4da55-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da55-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4da55-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da55-125">**запрос \_ ioctl \_ модулятор \_ Установка \_ активных \_ \_ циклов \_ активности**</span><span class="sxs-lookup"><span data-stu-id="4da55-125">**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




