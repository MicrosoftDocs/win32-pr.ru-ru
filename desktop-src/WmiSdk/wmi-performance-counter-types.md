---
description: Тип счетчика производительности обозначает формулу, необходимую для получения вычисляемых счетчиков производительности. Это те же типы счетчиков, которые используются в мониторинге производительности Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Типы счетчиков производительности WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155994"
---
# <a name="wmi-performance-counter-types"></a>Типы счетчиков производительности WMI

[Тип счетчика](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) производительности обозначает формулу, необходимую для получения вычисляемых счетчиков производительности. Это те же типы счетчиков, которые используются в [мониторинге производительности](/windows/desktop/PerfCtrs/performance-counters-portal)Windows. В классах производительности WMI необработанные данные для формулы типа счетчика берутся из класса [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , а вычисленный результат находится в свойстве с тем же именем соответствующего класса [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Типы счетчиков отображаются в качестве квалификатора **CounterType** для свойств в классах [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , а также в качестве квалификатора **Кукингтипе** для свойств в классах [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Например, свойство **авгдискбитесперреад** класса [**\_ \_ \_ LogicalDisk Win32 перфравдата перфдиск**](./retrieving-raw-and-formatted-performance-data.md) является необработанным источником данных для свойства **авгдискбитесперреад** в классе [**Win32 \_ перфформаттеддата \_ Перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), который содержит те же данные, что показаны в системном мониторе.

Следующий список упорядочивает описания типов счетчиков по функциональному типу:

-   [Базовые типы счетчиков](base-counter-types.md)
-   [Типы счетчиков базового алгоритма](basic-algorithm-counter-types.md)
-   [Типы счетчиков алгоритмов счетчиков](counter-algorithm-counter-types.md)
-   [Невычислительные типы счетчиков](noncomputational-counter-types.md)
-   [Типы счетчиков для алгоритма таймера точности](precision-timer-algorithm-counter-types.md)
-   [Типы счетчиков алгоритма длины очереди](queue-length-algorithm-counter-types.md)
-   [Типы статистических счетчиков](statistical-counter-types.md)
-   [Типы счетчиков алгоритмов таймера](timer-algorithm-counter-types.md)

 

 
