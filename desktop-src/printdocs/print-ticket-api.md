---
description: API билета печати позволяет приложениям управлять и преобразовывать билеты печати.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API билетов на печать
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac91cc976addba630bae3f250d244442ba1dd3b61f741575fe21cb250bab4a2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947802"
---
# <a name="print-ticket-api"></a>API билетов на печать

API билета печати позволяет приложениям управлять и преобразовывать билеты печати.

Билет на печать — это компонент документа XPS, который содержит предпочтительные параметры принтера для страницы в документе или для всего документа либо для задания печати, содержащего один или несколько документов. Обратите внимание, что билеты печати находятся только в документах XPS.

Прежде чем принтер сможет использовать билет печати, необходимо проверить билет печати на соответствие характеристикам принтера, определенным в функциях печати принтера. Приложение выполняет эту проверку, вызывая API билета печати.

PrintTicket и PrintCapabilities описываются с помощью элементов схемы печати, которая определяется [спецификацией печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Этот раздел содержит сведения о следующих элементах API:

-   [Функции API билетов на печать](print-ticket-api-functions.md)
-   [Перечисление API билетов на печать](print-ticket-api-enumerations.md)

на следующей схеме показана связь api билета печати с другими api-интерфейсами печати, которые может использовать собственное Windows приложение.

![Схема, показывающая связь API билета печати с другими API-интерфейсами печати, которые может использовать собственное приложение Windows](images/print-apis-pt.png)

## <a name="related-topics"></a>Связанные темы

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

 

 



