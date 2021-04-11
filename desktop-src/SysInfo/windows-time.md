---
description: Время Windows — это число миллисекунд, прошедших с момента последнего запуска системы.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Служба времени Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af776e2cc5a36993f6be0e0776d5b73fab6622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156130"
---
# <a name="windows-time"></a>Служба времени Windows

*Время Windows* — это число миллисекунд, прошедших с момента последнего запуска системы. Этот формат используется в основном для обратной совместимости с 16-разрядной системой Windows. Чтобы обеспечить успешное выполнение приложений, предназначенных для работы с 16-разрядной версией Windows, функция [**жеттикккаунт**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) возвращает текущее время Windows.

Как правило, функция [**жеттикккаунт**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) или [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) используется для сравнения текущего времени Windows с временем, возвращенным функцией [**жетмессажетиме**](/windows/win32/api/winuser/nf-winuser-getmessagetime) . **Жетмессажетиме** Возвращает время Windows, когда было создано указанное сообщение. **Жеттикккаунт** и **GetTickCount64** ограничены разрешением системного таймера, что составляет примерно 10 миллисекунд до 16 миллисекунд. Затраченное время, полученное **жеттикккаунт** или **GetTickCount64** , включает время, затрачиваемое системой в спящий режим или спящий режим.

Если требуется таймер более высокого разрешения, используйте функцию [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) , [таймер мультимедиа](/windows/desktop/Multimedia/multimedia-timers)или [таймер с высоким разрешением](../winmsg/about-timers.md). Затраченное время, полученное функцией **куерюнбиасединтеррупттиме** , включает только время, которое система тратит на рабочее состояние.

Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP/2000:** Функция [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) доступна начиная с Windows 7 и windows Server 2008 R2.

Счетчик производительности система времени ожидания можно использовать для получения количества секунд, прошедших с момента запуска компьютера. Этот счетчик производительности можно получить из данных о производительности в разделе реестра **hKey \_ Performance \_ Data**. Возвращаемое значение является 8-байтовым значением. Дополнительные сведения см. в статье [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
