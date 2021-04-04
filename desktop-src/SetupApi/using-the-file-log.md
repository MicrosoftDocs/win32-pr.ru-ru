---
description: Прежде чем можно будет использовать журнал файлов, необходимо вызвать Сетупинитиализефилелог, чтобы открыть или создать его. При вызове этой функции можно указать флаги для создания или перезаписи журнала файлов, открытия системного журнала или открытия журнала файлов с правами только для чтения.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Использование журнала файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999758"
---
# <a name="using-the-file-log"></a>Использование журнала файлов

Прежде чем можно будет использовать журнал файлов, необходимо вызвать [**сетупинитиализефилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) , чтобы открыть или создать его. При вызове этой функции можно указать флаги для создания или перезаписи журнала файлов, открытия системного журнала или открытия журнала файлов с правами только для чтения.

После того как [**сетупинитиализефилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) возвращает маркер в файл журнала, можно добавить запись, вызвав [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), удалить запись путем вызова [**сетупремовефилеложентри**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)или получить сведения о конкретном файле в журнале файлов, вызвав [**сетупкуерифилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).

Если файловый журнал больше не нужен, [**сетуптерминатефилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) должен быть вызван для освобождения ресурсов, выделенных во время вызова [**сетупинитиализефилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).

 

 



