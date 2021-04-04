---
description: Для работы с данными производительности в Visual Basic можно использовать следующие функции.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Функции счетчиков производительности для Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909720"
---
# <a name="performance-counters-functions-for-visual-basic"></a>Функции счетчиков производительности для Visual Basic

> [!IMPORTANT]
> Функции, описанные в этом разделе, могут быть изменены или недоступны в будущем. Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).

Для работы с данными производительности в Visual Basic можно использовать следующие функции.

- [**пдхклосекуери**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**пдхколлекткуеридата**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**пдхремовекаунтер**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**пдхвбаддкаунтер**](pdhvbaddcounter.md)
- [**пдхвбкреатекаунтерпаслист**](pdhvbcreatecounterpathlist.md)
- [**пдхвбжеткаунтерпаселементс**](pdhvbgetcounterpathelements.md)
- [**пдхвбжеткаунтерпасфромлист**](pdhvbgetcounterpathfromlist.md)
- [**пдхвбжетдаублекаунтервалуе**](pdhvbgetdoublecountervalue.md)
- [**пдхвбжетлогфилесизе**](pdhvbgetlogfilesize.md)
- [**пдхвбжетонекаунтерпас**](pdhvbgetonecounterpath.md)
- [**пдхвбисгудстатус**](pdhvbisgoodstatus.md)
- [**пдхвбопенлог**](pdhvbopenlog.md)
- [**пдхвбопенкуери**](pdhvbopenquery.md)
- [**пдхвбупдателог**](pdhvbupdatelog.md)

> [!NOTE]
> `PdhVb***`Функции работают с сеансом на уровне процесса и не являются потокобезопасными. Эти функции следует использовать только из простых однопотоковых приложений.
