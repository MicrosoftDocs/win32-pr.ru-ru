---
description: Определяет интервалы даты и времени с использованием формата, аналогичного синтаксису даты и времени, разбивая строку на поля для дней, часов, минут, секунд и микросекунд.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Формат интервала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647709"
---
# <a name="interval-format"></a><span data-ttu-id="183a9-103">Формат интервала</span><span class="sxs-lookup"><span data-stu-id="183a9-103">Interval Format</span></span>

<span data-ttu-id="183a9-104">WMI определяет интервалы даты и времени в формате, аналогичном синтаксису даты и времени, разбивая строку на поля для дней, часов, минут, секунд и микросекунд.</span><span class="sxs-lookup"><span data-stu-id="183a9-104">WMI defines date-time intervals with a format similar to the date and time syntax by breaking the string into the fields for days, hours, minutes, seconds, and microseconds.</span></span>

<span data-ttu-id="183a9-105">В следующем примере показан формат интервала даты-времени.</span><span class="sxs-lookup"><span data-stu-id="183a9-105">The following example shows the format of a date-time interval.</span></span>

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

<span data-ttu-id="183a9-106">В следующей таблице перечислены поля интервала даты-времени.</span><span class="sxs-lookup"><span data-stu-id="183a9-106">The following table lists the fields of the date-time interval.</span></span>



| <span data-ttu-id="183a9-107">Поле</span><span class="sxs-lookup"><span data-stu-id="183a9-107">Field</span></span>    | <span data-ttu-id="183a9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="183a9-108">Description</span></span>                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="183a9-109">dddddddd</span><span class="sxs-lookup"><span data-stu-id="183a9-109">dddddddd</span></span> | <span data-ttu-id="183a9-110">Восемь цифр, представляющих число дней (от 00000000 до 99999999).</span><span class="sxs-lookup"><span data-stu-id="183a9-110">Eight digits that represent a number of days (00000000 through 99999999).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="183a9-111">HH</span><span class="sxs-lookup"><span data-stu-id="183a9-111">HH</span></span>       | <span data-ttu-id="183a9-112">Двузначное число, обозначающее час дня, в котором используется 24-часовой формат (от 00 до 23).</span><span class="sxs-lookup"><span data-stu-id="183a9-112">Two-digit hour of the day that uses the 24-hour clock (00 through 23).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="183a9-113">ММ</span><span class="sxs-lookup"><span data-stu-id="183a9-113">MM</span></span>       | <span data-ttu-id="183a9-114">Двузначное число минут в час (от 00 до 59).</span><span class="sxs-lookup"><span data-stu-id="183a9-114">Two-digit minute in the hour (00 through 59).</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="183a9-115">SS</span><span class="sxs-lookup"><span data-stu-id="183a9-115">SS</span></span>       | <span data-ttu-id="183a9-116">Двузначное число секунд в минуте (от 00 до 59).</span><span class="sxs-lookup"><span data-stu-id="183a9-116">Two-digit number of seconds in the minute (00 through 59).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="183a9-117">мммммм</span><span class="sxs-lookup"><span data-stu-id="183a9-117">mmmmmm</span></span>   | <span data-ttu-id="183a9-118">Число микросекунд, состоящих из шести цифр, в секунду (000000 до 999999).</span><span class="sxs-lookup"><span data-stu-id="183a9-118">Six-digit number of microseconds in the second (000000 through 999999).</span></span> <span data-ttu-id="183a9-119">Ваша реализация не требуется для поддержки оценки с помощью этого поля, но это поле всегда должно присутствовать для сохранения природы строки фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="183a9-119">Your implementation is not required to support evaluation using this field, but this field must always be present to preserve the fixed-length nature of the string.</span></span> |



 

<span data-ttu-id="183a9-120">В качестве интервалов всегда следует использовать ": 000" в качестве последних четырех символов.</span><span class="sxs-lookup"><span data-stu-id="183a9-120">Intervals always have a trailing ":000" as the last four characters.</span></span> <span data-ttu-id="183a9-121">Кроме того, в отличие от даты и времени, нельзя использовать звездочки для указания неиспользуемых полей.</span><span class="sxs-lookup"><span data-stu-id="183a9-121">Further, unlike the date and time, you cannot use asterisks to indicate unused fields.</span></span> <span data-ttu-id="183a9-122">Кроме того, все свойства типа данных [CIM \_ DateTime](cim-datetime.md) , представляющие интервалы, должны быть помечены квалификатором "Стандартный" [подтипа](standard-wmi-qualifiers.md) , где для квалификатора задано значение "Interval".</span><span class="sxs-lookup"><span data-stu-id="183a9-122">In addition, all properties of type [CIM\_DATETIME](cim-datetime.md) that represent intervals must be marked with the [SubType](standard-wmi-qualifiers.md) standard qualifier, with the qualifier set to "interval".</span></span>

<span data-ttu-id="183a9-123">Следующая строка представляет интервал в 1 день, 12 часов, 0 минут и 32 секунд.</span><span class="sxs-lookup"><span data-stu-id="183a9-123">The following string represents an interval of 1 day, 12 hours, 0 minutes, and 32 seconds.</span></span>

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a><span data-ttu-id="183a9-124">См. также</span><span class="sxs-lookup"><span data-stu-id="183a9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="183a9-125">Формат даты и времени</span><span class="sxs-lookup"><span data-stu-id="183a9-125">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="183a9-126">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="183a9-126">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="183a9-127">\_Дата и время CIM</span><span class="sxs-lookup"><span data-stu-id="183a9-127">CIM\_DATETIME</span></span>](cim-datetime.md)
</dt> </dl>

 

 



