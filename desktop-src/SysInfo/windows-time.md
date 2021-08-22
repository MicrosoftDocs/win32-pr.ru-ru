---
description: время Windows — это число миллисекунд, прошедших с момента последнего запуска системы.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Служба времени Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363f455842a144decc9db7f4d15fa3353b16e74290252b911a814eb62832a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884050"
---
# <a name="windows-time"></a>Служба времени Windows

*время Windows* — это число миллисекунд, прошедших с момента последнего запуска системы. Этот формат существует в основном для обратной совместимости с 16-разрядной Windows. чтобы обеспечить успешную работу приложений, разработанных для 16-разрядных Windows, функция [**жеттикккаунт**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) возвращает текущее Windows время.

для сравнения текущего Windows времени с временем, возвращенным функцией [**жетмессажетиме**](/windows/win32/api/winuser/nf-winuser-getmessagetime) , обычно используется функция [**жеттикккаунт**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) или [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) . **жетмессажетиме** возвращает Windows время создания указанного сообщения. **Жеттикккаунт** и **GetTickCount64** ограничены разрешением системного таймера, что составляет примерно 10 миллисекунд до 16 миллисекунд. Затраченное время, полученное **жеттикккаунт** или **GetTickCount64** , включает время, затрачиваемое системой в спящий режим или спящий режим.

Если требуется таймер более высокого разрешения, используйте функцию [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) , [таймер мультимедиа](/windows/desktop/Multimedia/multimedia-timers)или [таймер с высоким разрешением](../winmsg/about-timers.md). Затраченное время, полученное функцией **куерюнбиасединтеррупттиме** , включает только время, которое система тратит на рабочее состояние.

**Windows server 2008, Windows Vista, Windows Server 2003 и Windows XP/2000:** функция [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) доступна начиная с Windows 7 и Windows Server 2008 R2.

Счетчик производительности система времени ожидания можно использовать для получения количества секунд, прошедших с момента запуска компьютера. Этот счетчик производительности можно получить из данных о производительности в разделе реестра **hKey \_ Performance \_ Data**. Возвращаемое значение является 8-байтовым значением. Дополнительные сведения см. в статье [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
