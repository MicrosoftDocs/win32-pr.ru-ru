---
description: Поставщик услуг необходим для создания одного или нескольких дескрипторов вызовов (переменных типа ХДРВКАЛЛ) всякий раз, когда TAPI вызывает одну из следующих функций.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Ожидающие обработки вызовы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d082c0b9111d6d58debacec01d20ffe9af2d024aafd61b3f1085267e62d3d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518593"
---
# <a name="pending-call-handles"></a>Ожидающие обработки вызовы

Поставщик услуг требуется для создания одного или нескольких дескрипторов вызова (переменных типа [хдрвкалл](hdrvline.md)) всякий раз, когда TAPI вызывает одну из этих функций: [**тспи \_ линемакекалл**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), [**тспи \_ линекомплететрансфер**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer), [**тспи \_ линефорвард**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward), [**Тспи \_ линепиккуп**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference), [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference), [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)и [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark). Когда поставщик услуг получает такой вызов, поставщик услуг должен установить переменную, предоставленную TAPI, в значение этого обработчика перед возвратом из вызова. TAPI считает, что этот "ожидающий обработки вызова" является предварительно допустимым. Когда поставщик услуг фактически создает вызов, он должен вызвать обратный вызов [**асинхронного \_ завершения**](/windows/win32/api/tspi/nc-tspi-async_completion) , чтобы формально проверить этот обработчик.

Если интерфейс TAPI вызывает функцию [**тспи \_ линеклосекалл**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) , прежде чем поставщик услуг формально проверит отложенный обработчик вызова, поставщик услуг должен завершить всю обработку, связанную с этим обработчиком вызова, и вызвать функцию обратного вызова [**асинхронного \_ завершения**](/windows/win32/api/tspi/nc-tspi-async_completion) , используя значение ошибки линирр \_ оператионфаилед.

 

 
