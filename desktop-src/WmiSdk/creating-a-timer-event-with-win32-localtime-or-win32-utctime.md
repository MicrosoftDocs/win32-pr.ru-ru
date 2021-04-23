---
description: Для получения уведомлений по времени можно использовать стандартную модель внутренних событий и фильтров событий в сочетании с \_ классами Win32 LocalTime или Win32 \_ утктиме.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Создание события таймера с Win32_LocalTime или Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272227"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a><span data-ttu-id="56314-103">Создание события таймера с помощью Win32 \_ LocalTime или Win32 \_ утктиме</span><span class="sxs-lookup"><span data-stu-id="56314-103">Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime</span></span>

<span data-ttu-id="56314-104">Для получения уведомлений по времени можно использовать стандартную модель внутренних событий и фильтров событий в сочетании с классами [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) или [**Win32 \_ утктиме**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) .</span><span class="sxs-lookup"><span data-stu-id="56314-104">You can use the standard model of intrinsic events and event filters in combination with the [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes to receive a timed notification.</span></span> <span data-ttu-id="56314-105">Внутренний метод является рекомендуемым способом создания событий с превышением времени, так как он согласуется с остальной моделью событий Майкрософт и поддерживает сложные условия планирования.</span><span class="sxs-lookup"><span data-stu-id="56314-105">The intrinsic method is a recommended way of generating timed events, as it is consistent with the rest of the Microsoft event model and supports complex scheduling conditions.</span></span>

<span data-ttu-id="56314-106">Классы [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) и [**Win32 \_ утктиме**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) — это Одноэлементные классы в корневом \\ пространстве имен CIMV2, представляющие системные часы.</span><span class="sxs-lookup"><span data-stu-id="56314-106">The [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) and [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes are singleton classes in the root\\cimv2 namespace that represent the system clock.</span></span> <span data-ttu-id="56314-107">При запросе **Win32 \_ localtime** возвращает текущее время на момент получения данных в 24-часовом формате с локальной ссылкой.</span><span class="sxs-lookup"><span data-stu-id="56314-107">When queried, **Win32\_LocalTime** returns the current time at the moment of data retrieval in a 24-hour clock with local reference.</span></span> <span data-ttu-id="56314-108">Класс **Win32 \_ утктиме** возвращает текущее время со ссылкой в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="56314-108">The **Win32\_UTCTime** class returns the current time with UTC reference.</span></span>

<span data-ttu-id="56314-109">**Создание событий времени или повторения с помощью Win32 \_ LocalTime или Win32 \_ утктиме**</span><span class="sxs-lookup"><span data-stu-id="56314-109">**To generate timed or repeating events with Win32\_LocalTime or Win32\_UTCTime**</span></span>

-   <span data-ttu-id="56314-110">Настройте встроенный фильтр событий уведомлений для [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) или [**Win32 \_ утктиме**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) , который запрашивает уведомление об определенной дате и времени.</span><span class="sxs-lookup"><span data-stu-id="56314-110">Set up an intrinsic notification event filter for [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) that requests notification for a specific date and time.</span></span>

<span data-ttu-id="56314-111">Например, если местное время перехода на летнее время равно 4 вечера.</span><span class="sxs-lookup"><span data-stu-id="56314-111">For example, if the local time under Daylight Savings Time is 4 P.M.</span></span> <span data-ttu-id="56314-112">а расположение — GMT-8, тогда [**Win32 \_ localtime. hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) возвращает 16 и [**Win32 \_ утктиме. hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) возвращает значение 23.</span><span class="sxs-lookup"><span data-stu-id="56314-112">and the location is GMT -8, then [**Win32\_LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) returns 16 and [**Win32\_UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) returns 23.</span></span>

<span data-ttu-id="56314-113">В следующем примере кода показано, как создать фильтр событий, который сигнализирует о повторении события каждый день в полночь.</span><span class="sxs-lookup"><span data-stu-id="56314-113">The following code example describes how to create an event filter that signals a repeating event every day at midnight.</span></span>

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
