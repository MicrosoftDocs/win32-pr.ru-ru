---
description: Отслеживание чисел отслеживает вызов цифр.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Отслеживание цифр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682540"
---
# <a name="digit-monitoring"></a><span data-ttu-id="ef1ee-103">Отслеживание цифр</span><span class="sxs-lookup"><span data-stu-id="ef1ee-103">Digit Monitoring</span></span>

<span data-ttu-id="ef1ee-104">Отслеживание чисел отслеживает вызов цифр.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-104">Digit monitoring monitors the call for digits.</span></span> <span data-ttu-id="ef1ee-105">TAPI позволяет получать сигналы цифр в соответствии с двумя методами (в цифровом режиме):</span><span class="sxs-lookup"><span data-stu-id="ef1ee-105">TAPI allows digits to be signaled according to two methods (digit modes):</span></span>

-   <span data-ttu-id="ef1ee-106">Числовые импульсы обозначаются как импульсные или роторные последовательности.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-106">Pulse Digits are signaled as pulse or rotary sequences.</span></span> <span data-ttu-id="ef1ee-107">При обнаружении эти импульсы переводятся как не только последовательности звуковых щелчков.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-107">For detection, these pulses manifest themselves as nothing more than sequences of audible clicks.</span></span> <span data-ttu-id="ef1ee-108">Допустимые разряды импульсов: от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-108">Valid pulse digits are '0' through '9'.</span></span>
-   <span data-ttu-id="ef1ee-109">Цифры DTMF получают сигналы DTMF (с двумя тонами с несколькими частотами).</span><span class="sxs-lookup"><span data-stu-id="ef1ee-109">DTMF Digits are signaled as DTMF (Dual Tone Multiple Frequency) tones.</span></span> <span data-ttu-id="ef1ee-110">Допустимые цифры DTMF: от 0 до 9, A.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-110">Valid DTMF digits are '0' through '9', 'A'.</span></span> <span data-ttu-id="ef1ee-111">"B", "C", "d", " \* " и " \# ".</span><span class="sxs-lookup"><span data-stu-id="ef1ee-111">'B', 'C', 'D', '\*', and '\#'.</span></span> <span data-ttu-id="ef1ee-112">Можно отслеживать как начало, так и нижнее края DTMF.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-112">Both the beginning and the down edge of DTMF digits can be monitored.</span></span>

<span data-ttu-id="ef1ee-113">Приложение может включать или отключать отслеживание чисел в указанном вызове с помощью [**линемонитордигитс**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span><span class="sxs-lookup"><span data-stu-id="ef1ee-113">An application can enable or disable digit monitoring on a specified call with [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span></span> <span data-ttu-id="ef1ee-114">Если отслеживание цифр включено, обнаруженные цифры приводят к тому, что приложение будет уведомлено с помощью [**строки \_ монитордигитс**](line-monitordigits.md) Message.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-114">When digit monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORDIGITS**](line-monitordigits.md) message.</span></span> <span data-ttu-id="ef1ee-115">Это сообщение предоставляет маркер вызова, в котором обнаружена цифра, а также цифровое значение и цифровой режим.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-115">This message provides the call handle on which the digit was detected as well as the digit value and the digit mode.</span></span> <span data-ttu-id="ef1ee-116">Область отслеживания чисел ограничивается временем существования вызова.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-116">The scope of digit monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="ef1ee-117">Отслеживание числа цифр в вызове завершается, как только вызов *отключается* или переходит в режим *простоя*.</span><span class="sxs-lookup"><span data-stu-id="ef1ee-117">Digit monitoring on a call ends as soon as the call *disconnects* or goes *idle*.</span></span>

 

 



