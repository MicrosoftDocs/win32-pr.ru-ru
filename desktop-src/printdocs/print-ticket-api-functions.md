---
description: Для управления билетами печати используются следующие функции.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Функции API билетов на печать
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5dfda941d0b0f7d99b0ffbef703a98e357ccc6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910795"
---
# <a name="print-ticket-api-functions"></a>Функции API билетов на печать

Для управления билетами печати используются следующие функции.

## <a name="in-this-section"></a>Содержание раздела



| Функция                                                                                  | Описание                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Преобразует структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в билет печати.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Преобразует билет печати в структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Выполняет слияние двух билетов на печать и возвращает допустимый, действующий билет печати.<br/>                                                                          |
| [**птклосепровидер**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Закрывает маркер поставщика билетов на печать.<br/>                                                                                                      |
| [**птконвертдевмодетопринттиккет**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Преобразует структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в билет печати внутри [**IStream**](/windows/desktop/Stg/istream-compound-file-implementation).<br/>        |
| [**птконвертпринттиккеттодевмоде**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Преобразует билет печати в структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                        |
| [**птжетпринткапабилитиес**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Получает возможности принтера, отформатированные в соответствии с XML- [схемой печати](./printschema.md).<br/>                   |
| [**птжетпринтдевицекапабилитиес**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Получает возможности принтера устройств, отформатированные в соответствии с XML- [схемой печати](./printschema.md).<br/>            |
| [**птжетпринтдевицересаурцес**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Он извлекает ресурсы печати устройств для принтера в соответствии со [схемой печати](./printschema.md)в формате XML.<br/> |
| [**птмержеандвалидатепринттиккет**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Выполняет слияние двух билетов на печать и возвращает допустимый, действующий билет печати.<br/>                                                                          |
| [**птопенпровидер**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Открывает экземпляр поставщика билетов на печать.<br/>                                                                                               |
| [**птопенпровидерекс**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Открывает экземпляр поставщика билетов на печать.<br/>                                                                                               |
| [**пткуерисчемаверсионсуппорт**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Возвращает самую новую (последнюю) версию [схемы печати](./printschema.md) , поддерживаемую указанным принтером.<br/>           |
| [**птрелеасемемори**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Освобождает буферы, связанные с билетами печати и возможностями печати.<br/>                                                                      |
| [**унбиндптпровидерсунк**](unbindptproviderthunk.md)<br/>                         | Закрывает маркер поставщика билетов на печать.<br/>                                                                                                 |



 

 

