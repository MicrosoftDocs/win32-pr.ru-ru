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
ms.openlocfilehash: f2dc2c3cbec2b87693920c0ed5ca113f7e6a04c9648f0ef2cc4bca9b4fa90f8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612414"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Создание события таймера с помощью Win32 \_ LocalTime или Win32 \_ утктиме

Для получения уведомлений по времени можно использовать стандартную модель внутренних событий и фильтров событий в сочетании с классами [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) или [**Win32 \_ утктиме**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) . Внутренний метод является рекомендуемым способом создания событий с превышением времени, так как он согласуется с остальной моделью событий Майкрософт и поддерживает сложные условия планирования.

Классы [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) и [**Win32 \_ утктиме**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) — это Одноэлементные классы в корневом \\ пространстве имен CIMV2, представляющие системные часы. При запросе **Win32 \_ localtime** возвращает текущее время на момент получения данных в 24-часовом формате с локальной ссылкой. Класс **Win32 \_ утктиме** возвращает текущее время со ссылкой в формате UTC.

**Создание событий времени или повторения с помощью Win32 \_ LocalTime или Win32 \_ утктиме**

-   Настройте встроенный фильтр событий уведомлений для [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) или [**Win32 \_ утктиме**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) , который запрашивает уведомление об определенной дате и времени.

Например, если местное время перехода на летнее время равно 4 вечера. а расположение — GMT-8, тогда [**Win32 \_ localtime. hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) возвращает 16 и [**Win32 \_ утктиме. hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) возвращает значение 23.

В следующем примере кода показано, как создать фильтр событий, который сигнализирует о повторении события каждый день в полночь.

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

 

 
