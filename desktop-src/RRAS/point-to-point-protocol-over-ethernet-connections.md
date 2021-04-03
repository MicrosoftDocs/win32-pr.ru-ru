---
title: протокол PPP через Ethernet подключения
description: Операционные системы Windows Server 2003, Windows XP и более поздних версий обеспечивают поддержку протокол PPP over Ethernet (PPPoE). Для подключения PPPoE задайте следующие значения в структуре РАСЕНТРИ.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987810"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>протокол PPP через Ethernet подключения

Операционные системы Windows Server 2003, Windows XP и более поздних версий обеспечивают поддержку протокол PPP over Ethernet (PPPoE). Для подключения PPPoE задайте следующие значения в структуре [**расентри**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .



| Член                      | Значение             |
|-----------------------------|-------------------|
| РАСЕНТРИ. Двтипе             | РАСЕТ \_ широкополосный доступ  |
| РАЕНТРИ. Сздевицетипе        | РАСДТ \_ PPPoE      |
| РАСЕНТРИ. Сзлокалфоненумбер | Имя службы. |



 

Чтобы задать эти значения, используйте функцию [**рассетентрипропертиес**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) .

Вы также можете использовать [**расентридлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) и флаг раседфлаг \_ невброадбандентри для [**расентридлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) , чтобы отобразить мастер для создания записи телефонной книги PPPoE.

 

 