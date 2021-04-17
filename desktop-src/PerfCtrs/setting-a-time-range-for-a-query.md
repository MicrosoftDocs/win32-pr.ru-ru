---
description: Если источником данных является файл журнала, можно указать диапазон времени для запроса.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Задание диапазона времени для запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663155"
---
# <a name="setting-a-time-range-for-a-query"></a>Задание диапазона времени для запроса

Если источником данных является файл журнала, можно указать диапазон времени для запроса. Запрос получает данные счетчика из файла журнала, собранного в течение заданного диапазона времени. Чтобы задать диапазон времени, вызовите функцию [**пдхсеткуеритимеранже**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) . **Пдхсеткуеритимеранже** не используется для запроса данных о производительности из источников данных в режиме реального времени.

Чтобы создать значение времени, выполните следующие действия.

1.  Выделите структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) и инициализируйте поля с нужным значением времени.
2.  Вызовите [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) , чтобы преобразовать значение времени структуры [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) в время структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
3.  Приведите структуру [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) как переменную лонглонг, учитывая соглашения о заполнении членов структуры платформы и компилятора.
4.  Скопируйте значение ЛОНГЛОНГ в соответствующее поле в структуре [**\_ \_ сведений о времени PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .

Чтобы получить диапазон времени всех данных о производительности, содержащихся в файле журнала, вызовите функцию [**пдхжетдатасаурцетимеранже**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .

 

 
