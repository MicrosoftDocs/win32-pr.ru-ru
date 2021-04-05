---
description: API билета печати позволяет приложениям управлять и преобразовывать билеты печати.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API билетов на печать
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104081734"
---
# <a name="print-ticket-api"></a>API билетов на печать

API билета печати позволяет приложениям управлять и преобразовывать билеты печати.

Билет на печать — это компонент документа XPS, который содержит предпочтительные параметры принтера для страницы в документе или для всего документа либо для задания печати, содержащего один или несколько документов. Обратите внимание, что билеты печати находятся только в документах XPS.

Прежде чем принтер сможет использовать билет печати, необходимо проверить билет печати на соответствие характеристикам принтера, определенным в функциях печати принтера. Приложение выполняет эту проверку, вызывая API билета печати.

PrintTicket и PrintCapabilities описываются с помощью элементов схемы печати, которая определяется [спецификацией печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Этот раздел содержит сведения о следующих элементах API:

-   [Функции API билетов на печать](print-ticket-api-functions.md)
-   [Перечисление API билетов на печать](print-ticket-api-enumerations.md)

На следующей схеме показана связь API билета печати с другими API-интерфейсами печати, которые может использовать собственное приложение Windows.

![Схема, показывающая связь API билета печати с другими API-интерфейсами печати, которые может использовать собственное приложение Windows](images/print-apis-pt.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[API печати XPS](xps-printing.md)
</dt> <dt>

[API диспетчера очереди печати](print-spooler-api.md)
</dt> <dt>

[API печати GDI](gdi-printing.md)
</dt> <dt>

[Печать спецификации схемы](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XPS](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



