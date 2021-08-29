---
description: В этом разделе описываются структуры, используемые с \_ функцией escape-функции мксдк и конвертером документов XPS (мксдк) (Майкрософт).
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: Структуры кода экранирования МКСДК
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b87ef962be9f8fffa1ae0b2d126cecfda4cc157118f4defd21360b030dc9d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948394"
---
# <a name="mxdc-escape-code-structures"></a>Структуры кода экранирования МКСДК

В этом разделе описываются структуры, используемые с функцией [**\_ escape**](mxdc-escape.md) -функции мксдк и конвертером документов XPS (Мксдк) (Майкрософт).

## <a name="in-this-section"></a>Содержание раздела



| Структура                                                                              | Описание                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**МКСДК \_ Escape- \_ заголовок \_ T**](mxdcescapeheader.md)<br/>                         | Структура [**мксдк \_ Escape \_ -заголовка \_ T**](/windows/desktop/printdocs/mxdcescapeheader) содержит код операции для вызова [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с [**\_ escape-мксдк**](mxdc-escape.md) в качестве параметра *нескапе* . Он также предоставляет размеры входных и выходных буферов.<br/>  |
| [**МКСДК \_ получить \_ данные имени файла \_ \_ T**](mxdcgetfilenamedata.md)<br/>                 | Структура [**мксдк \_ Get \_ filename \_ Data \_ T**](/windows/desktop/printdocs/mxdcgetfilenamedata) содержит полный путь и имя выходного файла конвертера документов Microsoft XPS (мксдк).<br/>                                                                                                     |
| [**\_Escape- \_ последовательность мксдк PRINTTICKET \_ T**](mxdcprintticketescape.md)<br/>               | Структура [**\_ Escape- \_ последовательности мксдк PRINTTICKET \_ t**](mxdcprintticketescape.md) представляет собой [**мксдкную структуру \_ \_ заголовка \_ t**](mxdcescapeheader.md) , объединяющую [**структуру \_ данных мксдк PrintTicket \_ \_ t**](mxdcprintticketpassthrough.md) .<br/>                            |
| [**МКСДК \_ \_ данных PRINTTICKET \_ T**](mxdcprintticketpassthrough.md)<br/>            | Структура [**\_ данных мксдк \_ PRINTTICKET \_**](/windows/desktop/printdocs/mxdcprintticketpassthrough) содержит билет на печать документа XPS, который содержит параметры принтера и печати, для передачи в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.<br/>              |
| [**МКСДК \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md)<br/>                             | Структура [**\_ данных мксдк \_ S0PAGE \_**](/windows/desktop/printdocs/mxdcs0pagedata) содержит страницу документа XPS, которая передается в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.<br/>                                                                                  |
| [**МКСДК \_ S0PAGE \_ сквозной \_ escape-последовательности \_ T**](mxdcs0pagepassthroughescape.md)<br/> | [**Мксдк \_ S0PAGE \_ сквозная \_ Структура \_ t**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape) представляет собой структуру [**escape-последовательности мксдк \_ \_ \_ t**](mxdcescapeheader.md) , объединенную с структурой [**мксдк \_ S0PAGE \_ Data \_ t**](mxdcs0pagedata.md) .<br/>                             |
| [**\_Escape- \_ последовательность ресурсов мксдк S0PAGE \_ \_ T**](mxdcs0pageresourceescape.md)<br/>       | Escape-структура [**\_ \_ ресурса \_ мксдк \_ S0PAGE**](/windows/desktop/printdocs/mxdcs0pageresourceescape) представляет собой структуру [**\_ \_ \_ t мксдк**](mxdcescapeheader.md) ~, объединенную с структурой [**мксдк \_ XPS \_ S0PAGE \_ Resource \_ t**](mxdcxpss0pageresource.md) .<br/>                   |
| [**МКСДК \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md)<br/>             | Структура [**мксдк \_ XPS \_ S0PAGE \_ Resource \_ T**](/windows/desktop/printdocs/mxdcxpss0pageresource) содержит сведения о ресурсе, например изображение или шрифт, который связан со страницей документа XPS и передается в выходной файл конвертера документов Microsoft XPS (мксдк).<br/> |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Escape-МКСДК \_**](mxdc-escape.md)
</dt> </dl>

 

