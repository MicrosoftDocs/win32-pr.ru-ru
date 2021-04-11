---
description: Содержит текущий процент циклов работоспособности для ПИН-кода или канала в контроллере широты импульсов.
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: Структура PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT (широт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141499"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a><span data-ttu-id="4e8d9-103">Закрепление широтного импульса \_ \_ Получение \_ активной \_ \_ \_ процентной структуры циклов пошлины \_</span><span class="sxs-lookup"><span data-stu-id="4e8d9-103">PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT structure</span></span>

<span data-ttu-id="4e8d9-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4e8d9-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4e8d9-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4e8d9-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4e8d9-106">Содержит текущий процент циклов работоспособности для ПИН-кода или канала в контроллере широты импульсов.</span><span class="sxs-lookup"><span data-stu-id="4e8d9-106">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e8d9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e8d9-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="4e8d9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4e8d9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e8d9-109">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="4e8d9-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="4e8d9-110">Текущий цикл обработки сигнала ШИРОТы в виде коэффициента ШИРОТы в \_ процентах (улонглонг).</span><span class="sxs-lookup"><span data-stu-id="4e8d9-110">The current PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e8d9-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4e8d9-111">Requirements</span></span>



| <span data-ttu-id="4e8d9-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4e8d9-112">Requirement</span></span> | <span data-ttu-id="4e8d9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4e8d9-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e8d9-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e8d9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4e8d9-115">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4e8d9-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e8d9-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e8d9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4e8d9-117">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="4e8d9-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4e8d9-118">Минимальная версия КМДФ</span><span class="sxs-lookup"><span data-stu-id="4e8d9-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="4e8d9-119">1,19</span><span class="sxs-lookup"><span data-stu-id="4e8d9-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="4e8d9-120">Минимальная версия UMDF</span><span class="sxs-lookup"><span data-stu-id="4e8d9-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="4e8d9-121">2.19</span><span class="sxs-lookup"><span data-stu-id="4e8d9-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="4e8d9-122">Header</span><span class="sxs-lookup"><span data-stu-id="4e8d9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e8d9-123"><dt>Широт. h (включая широту. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e8d9-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e8d9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e8d9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e8d9-125">**IOCTL \_ широтного \_ ПИН-кода \_ Получение \_ активной \_ пошлины в \_ \_ процентах**</span><span class="sxs-lookup"><span data-stu-id="4e8d9-125">**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




