---
description: 'Дополнительные сведения о: структуры ШИРОТы'
ms.assetid: 992E3913-C1C4-48C1-A550-475CF44AB065
title: Структуры ШИРОТы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99511820f8500cd8df827a80664f6c274d732665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990519"
---
# <a name="pwm-structures"></a><span data-ttu-id="76282-103">Структуры ШИРОТы</span><span class="sxs-lookup"><span data-stu-id="76282-103">PWM Structures</span></span>

<span data-ttu-id="76282-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="76282-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="76282-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="76282-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="76282-106">При модуляции с заданной шириной импульсов используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="76282-106">The following structures are used with Pulse Width Modulation:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="76282-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="76282-107">In this section</span></span>



| <span data-ttu-id="76282-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="76282-108">Topic</span></span>                                                                                                                        | <span data-ttu-id="76282-109">Описание</span><span class="sxs-lookup"><span data-stu-id="76282-109">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76282-110">**контроллер широтного модулятора \_ \_ Получение \_ данных фактического \_ периода \_**</span><span class="sxs-lookup"><span data-stu-id="76282-110">**PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT**</span></span>](pwm-controller-get-actual-period-output.md)<br/>                   | <span data-ttu-id="76282-111">Содержит действующий период вывода сигнала для контроллера ШИРОТы импульсов.</span><span class="sxs-lookup"><span data-stu-id="76282-111">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span><br/>                    |
| [<span data-ttu-id="76282-112">**\_сведения о контроллере широты \_**</span><span class="sxs-lookup"><span data-stu-id="76282-112">**PWM\_CONTROLLER\_INFO**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_info)<br/>                                                              | <span data-ttu-id="76282-113">Представляет статическую информацию, которая характеризует контроллер ШИРОТы импульсов.</span><span class="sxs-lookup"><span data-stu-id="76282-113">Represents the static information that characterizes a Pulse Width Modulation (PWM) controller.</span></span> <br/>              |
| [<span data-ttu-id="76282-114">**\_ \_ \_ Ввод требуемого периода для контроллера модуляторных \_ \_ данных**</span><span class="sxs-lookup"><span data-stu-id="76282-114">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_input)<br/>                   | <span data-ttu-id="76282-115">Содержит входное значение для рекомендуемого периода сигнала для контроллера ШИРОТы импульсов.</span><span class="sxs-lookup"><span data-stu-id="76282-115">Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller.</span></span> <br/>       |
| [<span data-ttu-id="76282-116">**\_ \_ \_ выходные данные требуемого \_ периода \_ для контроллера модуляторов**</span><span class="sxs-lookup"><span data-stu-id="76282-116">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_OUTPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_output)<br/>                 | <span data-ttu-id="76282-117">Содержит действующий период вывода сигнала контроллера широты импульсов.</span><span class="sxs-lookup"><span data-stu-id="76282-117">Contains the effective output signal period of the Pulse Width Modulation (PWM) controller.</span></span><br/>                   |
| [<span data-ttu-id="76282-118">**закрепление ШИРОТного \_ закрепления — \_ Получение \_ \_ \_ \_ процентных \_ результатов активной пошлины**</span><span class="sxs-lookup"><span data-stu-id="76282-118">**PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT**</span></span>](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/> | <span data-ttu-id="76282-119">Содержит текущий процент циклов работоспособности для ПИН-кода или канала в контроллере широты импульсов.</span><span class="sxs-lookup"><span data-stu-id="76282-119">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/> |
| [<span data-ttu-id="76282-120">**\_процент ввода-закрепления для \_ \_ активного \_ цикла пошлины \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="76282-120">**PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT**</span></span>](pwm-pin-set-active-duty-cycle-percentage-input.md)<br/>   | <span data-ttu-id="76282-121">Содержит требуемый процент циклов пошлины для ПИН-кода или канала в контроллере широты импульсов.</span><span class="sxs-lookup"><span data-stu-id="76282-121">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/>   |
| [<span data-ttu-id="76282-122">**выход ШИРОТного \_ ПИН-кода \_ Получение \_ данных о полярности \_**</span><span class="sxs-lookup"><span data-stu-id="76282-122">**PWM\_PIN\_GET\_POLARITY\_OUTPUT**</span></span>](pwm-pin-get-polarity-output.md)<br/>                                            | <span data-ttu-id="76282-123">Содержит значение полярности для возврата.</span><span class="sxs-lookup"><span data-stu-id="76282-123">Contains a polarity value to return.</span></span><br/>                                                                          |
| [<span data-ttu-id="76282-124">**\_ \_ \_ входные данные полярности для набора закрепления \_**</span><span class="sxs-lookup"><span data-stu-id="76282-124">**PWM\_PIN\_SET\_POLARITY\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input)<br/>                                              | <span data-ttu-id="76282-125">Содержит требуемое значение для полярности ПИН-кода или канала.</span><span class="sxs-lookup"><span data-stu-id="76282-125">Contains a desired value for polarity of a pin or channel.</span></span><br/>                                                    |
| [<span data-ttu-id="76282-126">**\_выходное закрепление широтного ПИН-кода \_ \_ запущено \_**</span><span class="sxs-lookup"><span data-stu-id="76282-126">**PWM\_PIN\_IS\_STARTED\_OUTPUT**</span></span>](pwm-pin-is-started-output.md)<br/>                                                | <span data-ttu-id="76282-127">Содержит текущее состояние создания сигнала для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="76282-127">Contains the current signal generation state of a pin.</span></span><br/>                                                        |



 

 

 




