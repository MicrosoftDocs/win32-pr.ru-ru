---
description: Узнайте, как автор клиента PrintTicket может использовать типы элементов для создания PrintTicket, который описывает цель для устройства.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Контрольные списки для создания PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76d47911d0060cc6d06604bfaeaa4abcebd3daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405477"
---
# <a name="printticket-construction-checklists"></a>Контрольные списки для создания PrintTicket

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

В этом разделе показано, как автор клиента PrintTicket может использовать типы элементов, определенные в платформе схемы печати, для создания PrintTicket, который описывает цель для устройства. PrintTicket может быть универсальным (не привязанным к конкретному устройству) или может быть специфичным для конкретного устройства. Семантика PrintTicket представлена более подробно. Кроме того, этот раздел содержит общие сведения о концепциях и терминологии, более подробно описанные в последующих разделах.

Существует два принципиально различных подхода к построению PrintTicket. Можно использовать любой из этих подходов.

-   Нацеливание PrintTicket на неизвестное или универсальное устройство, [создав универсальный PrintTicket](creating-a-generic-printticket.md).

    Если ваша основная цель — сохранить намерение конечного пользователя, можно воспользоваться этим подходом, создав и сохранив непроверенный универсальный PrintTicket с документом.

-   Нацеливание PrintTicket на определенное устройство путем [создания Device-Specific PrintTicket](creating-a-device-specific-printticket.md).

    Если вы больше заинтересованы в использовании всех функций, предлагаемых определенным устройством, можно воспользоваться этим подходом, создав PrintTicket для конкретного устройства и сохранив проверенный PrintTicket в документе.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



