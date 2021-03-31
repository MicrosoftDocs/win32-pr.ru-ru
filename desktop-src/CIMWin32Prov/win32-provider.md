---
description: Microsoft&\# 160; Поставщик Win32 извлекает и обновляет данные, относящиеся к системам Windows&\# 8212; такие данные, как текущие параметры переменных среды и атрибуты логического диска.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Поставщик Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807078"
---
# <a name="win32-provider"></a>Поставщик Win32

Поставщик Microsoft Win32 извлекает и обновляет данные, относящиеся к системам Windows — такие данные, как текущие параметры переменных среды и атрибуты логического диска. С помощью поставщика Win32 приложения управления могут использовать инструментарий WMI для простого доступа к этим данным. Поставщик Win32 извлекает свои данные, делая вызов функций Windows и запрашивая системный реестр.

Поставщик Win32 определяет классы, используемые для описания оборудования или программного обеспечения, доступного в системах Windows, и связи между ними.

Как экземпляр и поставщик методов, поставщик Win32 реализует стандартный интерфейс [**ивбемпровидеринит**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) , а также следующие методы [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) :

-   [**креатеинстанцеенумасинк**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**делетеинстанцеасинк**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ексекмесодасинк**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ексеккуерясинк**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**жетобжектасинк**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**путинстанцеасинк**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

В следующей таблице перечислены категории классов поставщиков Win32.



| Классы                                                                             | Описание                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Аппаратные классы системы компьютера](computer-system-hardware-classes.md)<br/> | Объекты, связанные с оборудованием.<br/>                                      |
| [Классы операционной системы](operating-system-classes.md)<br/>                 | Объекты, связанные с операционной системой.<br/>                              |
| [Классы счетчиков производительности](performance-counter-classes.md)<br/>           | Необработанные и вычисленные данные производительности из счетчиков производительности.<br/> |
| [Классы управления службами WMI](wmi-service-management-classes.md)<br/>     | Управление для WMI.<br/>                                            |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поставщик WMI CIMWin32](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
