---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Контрольные списки для создания PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693892"
---
# <a name="printticket-construction-checklists"></a>Контрольные списки для создания PrintTicket

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

В этом разделе показано, как автор клиента PrintTicket может использовать типы элементов, определенные в платформе схемы печати, для создания PrintTicket, который описывает цель для устройства. PrintTicket может быть универсальным (не привязанным к конкретному устройству) или может быть специфичным для конкретного устройства. Семантика PrintTicket представлена более подробно. Кроме того, этот раздел содержит общие сведения о концепциях и терминологии, более подробно описанные в последующих разделах.

Существует два принципиально различных подхода к построению PrintTicket. Можно использовать любой из этих подходов.

-   Нацеливание PrintTicket на неизвестное или универсальное устройство, [создав универсальный PrintTicket](creating-a-generic-printticket.md).

    Если ваша основная цель — сохранить намерение конечного пользователя, можно воспользоваться этим подходом, создав и сохранив непроверенный универсальный PrintTicket с документом.

-   Нацеливание PrintTicket на определенное устройство путем [создания Device-Specific PrintTicket](creating-a-device-specific-printticket.md).

    Если вы больше заинтересованы в использовании всех функций, предлагаемых определенным устройством, можно воспользоваться этим подходом, создав PrintTicket для конкретного устройства и сохранив проверенный PrintTicket в документе.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



