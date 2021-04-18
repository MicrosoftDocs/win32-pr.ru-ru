---
description: Предоставляет интерфейс диспетчера очереди печати. Приложения могут использовать этот API для отправки XPS-документов на принтер.
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: API печати XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711684"
---
# <a name="xps-print-api"></a>API печати XPS

\[API печати XPS не поддерживается и может быть изменен или недоступен в будущем. Вместо этого клиентские приложения должны использовать [API пакета печати документов](./tailored-app-printing-api.md) .\]

Предоставляет интерфейс диспетчера очереди печати. Приложения могут использовать этот API для отправки XPS-документов на принтер.

В этом разделе содержатся сведения о следующих разделах.

<dl>

[Сведения об API печати XPS](about-xps-print-api.md)  
[Использование API печати XPS](using-the-xps-print-api.md)  
[Справочник по API печати XPS](xpsprint-interfaces.md)  
</dl>

Собственные приложения Windows, которые создают документы XPS, например, с помощью [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)), могут использовать API печати XPS для отправки содержимого XPS-документа на принтер.

На следующей схеме показана связь API печати XPS с другими интерфейсами API печати, которые может использовать собственное приложение Windows.

![Схема, показывающая связь API печати XPS с другими интерфейсами API печати, которые может использовать собственное приложение Windows](images/print-apis-xps.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[API диспетчера очереди печати](print-spooler-api.md)
</dt> <dt>

[API билетов на печать](print-ticket-api.md)
</dt> <dt>

[API печати GDI](gdi-printing.md)
</dt> </dl>

 

 
