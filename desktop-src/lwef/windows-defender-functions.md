---
title: Защитник Windows Функции
description: функции, вызываемые приложениями для запроса сканирования, обновлений сигнатур или сведений из Защитник Windows.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ecfa00a38c2263fe1db1b996bb3ec052f8caef1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483130"
---
# <a name="windows-defender-functions"></a>Защитник Windows Функции

функции, вызываемые приложениями для запроса сканирования, обновлений сигнатур или сведений из Защитник Windows.




| Компонент | Описание | 
|----------|-------------|
| <a href="mperrormessageformat.md"><strong>мперрормессажеформат</strong></a> | Возвращает отформатированное сообщение об ошибке на основе кода ошибки.<br /> | 
| <a href="mpfreememory.md"><strong>мпфримемори</strong></a> | Освобождает память для диспетчера защиты от вредоносных программ.<br /> | 
| <a href="mphandleclose.md"><strong>мфандлеклосе</strong></a> | Закрывает маркер, возвращенный <a href="mpmanageropen.md"><strong>мпманажеропен</strong></a>, <a href="mpscanstart.md"><strong>мпсканстарт</strong></a>, <a href="mpthreatopen.md"><strong>мпсреатопен</strong></a>или <a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a>.<br /> | 
| <a href="mpmanageropen.md"><strong>мпманажеропен</strong></a> | Устанавливает подключение к диспетчеру защиты от вредоносных программ на локальном компьютере.<br /> | 
| <a href="mpmanagerstatusquery.md"><strong>мпманажерстатускуери</strong></a> | <strong>Не поддерживается</strong> Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ.<br /> | 
| <a href="mpmanagerstatusqueryex.md"><strong>мпманажерстатускуерекс</strong></a> | Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ.<br /> | 
| <a href="mpmanagerversionquery.md"><strong>мпманажерверсионкуери</strong></a> | Возвращает сведения о версии различных компонентов диспетчера защиты от вредоносных программ.<br /> | 
| <a href="mpscancontrol.md"><strong>мпсканконтрол</strong></a> | Разрешает Управление сканированием, которое было асинхронно инициировано через <a href="mpscanstart.md"><strong>мпсканстарт</strong></a>.<br /> | 
| <a href="mpscanstart.md"><strong>мпсканстарт</strong></a> | Запускает операцию сканирования.<br /> | 
| <a href="mpthreatenumerate.md"><strong>мпсреатенумерате</strong></a> | Возвращает сведения о следующей угрозе в списке перечисления. Эту функцию можно вызывать повторно до тех пор, пока не завершится перечисление всех угроз.<br /> | 
| <a href="mpthreatopen.md"><strong>мпсреатопен</strong></a> | Возвращает маркер перечисления, предназначенный для получения угроз. Эта функция может использоваться для открытия угроз, обнаруженных конкретным сканированием, всех активных угроз в системе, истории заражения угроз или всех угроз, имеющихся в базе данных сигнатур.<br /> | 
| <a href="mpthreatquery.md"><strong>мпсреаткуери</strong></a> | Используется для запроса статических (таких как серьезность и категория) или локализованных сведений о конкретной угрозе (например, описание категории и рекомендации).<br /> | 
| <a href="mpupdatecontrol.md"><strong>мпупдатеконтрол</strong></a> | Позволяет управлять операцией обновления сигнатур, которая была асинхронно инициирована через <a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a>.<br /> | 
| <a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a> | Запускает операцию обновления сигнатур.<br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>вденабле</strong></a> | изменяет состояние Защитник Windows на вкл или выкл.<br /><blockquote>[!Note]<br />начиная с Windows 10, версии 1607 и Windows Server 2016 функция <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>вденабле</strong></a> всегда возвращает <strong>E_NOTIMPL</strong>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>вдстатус</strong></a> | возвращает текущее состояние Защитник Windows.<br /> | 




 

 

 





