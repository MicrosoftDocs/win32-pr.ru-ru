---
description: Содержит значение полярности для возврата.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Структура PWM_PIN_GET_POLARITY_OUTPUT (широт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990520"
---
# <a name="pwm_pin_get_polarity_output-structure"></a><span data-ttu-id="bb3c8-103">\_Схема \_ \_ \_ вывода данных о полярности с модулятором</span><span class="sxs-lookup"><span data-stu-id="bb3c8-103">PWM\_PIN\_GET\_POLARITY\_OUTPUT structure</span></span>

<span data-ttu-id="bb3c8-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bb3c8-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="bb3c8-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bb3c8-106">Содержит значение полярности для возврата.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-106">Contains a polarity value to return.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3c8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb3c8-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="bb3c8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="bb3c8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb3c8-109">**Полярность**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-109">**Polarity**</span></span>
</dt> <dd>

<span data-ttu-id="bb3c8-110">Полярность ПИН-кода или канала в виде значения [**\_ полярности широты**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .</span><span class="sxs-lookup"><span data-stu-id="bb3c8-110">The polarity of the pin or channel as a [**PWM\_POLARITY**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) value.</span></span> <span data-ttu-id="bb3c8-111">Значение полярности — "активный" или "низкий".</span><span class="sxs-lookup"><span data-stu-id="bb3c8-111">The polarity is either Active High or Active Low.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb3c8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="bb3c8-112">Requirements</span></span>



| <span data-ttu-id="bb3c8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="bb3c8-113">Requirement</span></span> | <span data-ttu-id="bb3c8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bb3c8-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3c8-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb3c8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bb3c8-116">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bb3c8-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb3c8-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb3c8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bb3c8-118">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="bb3c8-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bb3c8-119">Минимальная версия КМДФ</span><span class="sxs-lookup"><span data-stu-id="bb3c8-119">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="bb3c8-120">1,19</span><span class="sxs-lookup"><span data-stu-id="bb3c8-120">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="bb3c8-121">Минимальная версия UMDF</span><span class="sxs-lookup"><span data-stu-id="bb3c8-121">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="bb3c8-122">2.19</span><span class="sxs-lookup"><span data-stu-id="bb3c8-122">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="bb3c8-123">Header</span><span class="sxs-lookup"><span data-stu-id="bb3c8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb3c8-124"><dt>Широт. h (включая широту. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb3c8-124"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb3c8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb3c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb3c8-126">**IOCTL \_ широтного \_ ПИН-кода \_ Получение \_ полярности**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-126">**IOCTL\_PWM\_PIN\_GET\_POLARITY**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[<span data-ttu-id="bb3c8-127">**\_полярность широты**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-127">**PWM\_POLARITY**</span></span>](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

