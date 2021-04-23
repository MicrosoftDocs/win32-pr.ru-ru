---
description: Модулятор по ширине импульсов (широты) — это способ создания прямоугольной импульсной волновой волны с заданной толщиной импульса, которая приводит к получению варианта среднего значения звукового сигнала.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: API-ИНТЕРФЕЙС ШИРОТЫ
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538885"
---
# <a name="pwm-api"></a><span data-ttu-id="4f6af-103">API-ИНТЕРФЕЙС ШИРОТЫ</span><span class="sxs-lookup"><span data-stu-id="4f6af-103">PWM API</span></span>

<span data-ttu-id="4f6af-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4f6af-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4f6af-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4f6af-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4f6af-106">Модулятор по ширине импульсов (широты) — это способ создания прямоугольной импульсной волновой волны с заданной толщиной импульса, которая приводит к получению варианта среднего значения звукового сигнала.</span><span class="sxs-lookup"><span data-stu-id="4f6af-106">Pulse Width Modulation (PWM) is the technique of generating a rectangular pulse wave that has a pulse width that is modulated to result in the variation of the average value of the waveform.</span></span> <span data-ttu-id="4f6af-107">Наиболее распространенные применения включают в себя серво моторы, индикаторы DIMM или другие связанные функции.</span><span class="sxs-lookup"><span data-stu-id="4f6af-107">Most common uses include driving servo motors, dimming LEDs, or other related functions.</span></span> <span data-ttu-id="4f6af-108">Модулятор предназначен для использования в основном для Интернет вещей сценариев.</span><span class="sxs-lookup"><span data-stu-id="4f6af-108">PWM is intended to be used primarily for Internet of Things scenarios.</span></span>

## <a name="about-pulse-width-modulation"></a><span data-ttu-id="4f6af-109">О модуляции для импульсной ширины</span><span class="sxs-lookup"><span data-stu-id="4f6af-109">About Pulse Width Modulation</span></span>

<span data-ttu-id="4f6af-110">С помощью форм-волнового ИМПУЛЬСа можно разделить два параметра:</span><span class="sxs-lookup"><span data-stu-id="4f6af-110">A PWM waveform can be categorized by two parameters:</span></span>

-   <span data-ttu-id="4f6af-111">Период волны (T)</span><span class="sxs-lookup"><span data-stu-id="4f6af-111">A waveform period (T)</span></span>

-   <span data-ttu-id="4f6af-112">Цикл пошлины, где частота сигнала (f) является обратной точкой f = 1/T</span><span class="sxs-lookup"><span data-stu-id="4f6af-112">The duty cycle, where the waveform frequency (f) is the reciprocal of the period f=1/T</span></span>

<span data-ttu-id="4f6af-113">Цикл пошлины описывает пропорции  / **активного** времени по отношению к обычному интервалу или **периоду** времени.</span><span class="sxs-lookup"><span data-stu-id="4f6af-113">The duty cycle describes the proportion of the **on**/**Active** time with respect to the regular interval or **Period** of time.</span></span> <span data-ttu-id="4f6af-114">Цикл с низкой нагрузкой соответствует среднему времени низкой выходной мощности, так как в большинстве случаев выключение питания отключено.</span><span class="sxs-lookup"><span data-stu-id="4f6af-114">A low duty cycle corresponds to an average of low output power, because the power is off for most of the time.</span></span> <span data-ttu-id="4f6af-115">Цикл пошлины выражается в процентах.</span><span class="sxs-lookup"><span data-stu-id="4f6af-115">Duty cycle is expressed as a percentage.</span></span> <span data-ttu-id="4f6af-116">Полностью включено — 100%.</span><span class="sxs-lookup"><span data-stu-id="4f6af-116">Fully on is 100%.</span></span> <span data-ttu-id="4f6af-117">Полностью отключено — 0%.</span><span class="sxs-lookup"><span data-stu-id="4f6af-117">Fully off is 0%.</span></span> <span data-ttu-id="4f6af-118">**Активная** половина времени — 50%.</span><span class="sxs-lookup"><span data-stu-id="4f6af-118">**Active** half the time is 50%.</span></span>

<span data-ttu-id="4f6af-119">Разработчикам, желающим реализовать ШИРОТу в своих приложениях IoT, следует изучить [документацию по широте для WinRT.](/uwp/api/windows.devices.pwm)</span><span class="sxs-lookup"><span data-stu-id="4f6af-119">Developers looking to implement PWM in their IoT applications should investigate the [WinRT PWM documentation.](/uwp/api/windows.devices.pwm)</span></span>

## <a name="pulse-width-modulation-types"></a><span data-ttu-id="4f6af-120">Типы модуляции для импульсной ширины</span><span class="sxs-lookup"><span data-stu-id="4f6af-120">Pulse Width Modulation types</span></span>

<span data-ttu-id="4f6af-121">ШИРОТа использования [этих кодов управления вводом-вывода](pwm-control-codes.md), [структур](pwm-structures.md)и [перечислений.](pwm-enumeration-types.md)</span><span class="sxs-lookup"><span data-stu-id="4f6af-121">PWM uses [these IO control codes](pwm-control-codes.md), [structures](pwm-structures.md), and [enumerations.](pwm-enumeration-types.md)</span></span>

<span data-ttu-id="4f6af-122">В модулятор также используется следующая функция: [**пвмпарсепинпас**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span><span class="sxs-lookup"><span data-stu-id="4f6af-122">PWM also uses the following function: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span></span>

 

 
