---
title: протокол PPP через Ethernet подключения
description: Windows сервер 2003, Windows XP и более поздние операционные системы обеспечивают поддержку протокол PPP по протоколу Ethernet (PPPoE). Для подключения PPPoE задайте следующие значения в структуре РАСЕНТРИ.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92703bac13d129ed29cee1c22328825de67325239c1906c1728b96d53398647b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789814"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>протокол PPP через Ethernet подключения

Windows сервер 2003, Windows XP и более поздние операционные системы обеспечивают поддержку протокол PPP по протоколу Ethernet (PPPoE). Для подключения PPPoE задайте следующие значения в структуре [**расентри**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .



| Член                      | Значение             |
|-----------------------------|-------------------|
| РАСЕНТРИ. Двтипе             | РАСЕТ \_ широкополосный доступ  |
| РАЕНТРИ. Сздевицетипе        | РАСДТ \_ PPPoE      |
| РАСЕНТРИ. Сзлокалфоненумбер | Имя службы. |



 

Чтобы задать эти значения, используйте функцию [**рассетентрипропертиес**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) .

Вы также можете использовать [**расентридлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) и флаг раседфлаг \_ невброадбандентри для [**расентридлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) , чтобы отобразить мастер для создания записи телефонной книги PPPoE.

 

 