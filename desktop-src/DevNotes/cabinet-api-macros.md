---
description: 'Дополнительные сведения: макросы API CAB-файла'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Макросы API CAB-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525ec84e3e857c4819b1689cade2ed0f7267dffbd8a0e0da02251a03f8d4a36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668272"
---
# <a name="cabinet-api-macros"></a>Макросы API CAB-файла

В этом разделе описываются макросы, используемые API CAB-файлов:

## <a name="fci-macros"></a>FCI макросы

FCI использует следующие макросы:



| Макрос                                              | Описание                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**фнфЦиаллок**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Используется для выделения памяти в контексте FCI.<br/>                                          |
| [**фнфЦиклосе**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Используется для закрытия файла.<br/>                                                               |
| [**фнфЦиделете**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Используется для удаления файла.<br/>                                                              |
| [**фнфЦифилеплацед**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Используется для уведомления о помещении файла в CAB-файл.<br/>                                |
| [**фнфЦифри**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Используется для высвобождения ранее выделенной памяти в контексте FCI.<br/>                         |
| [**фнфЦижетнексткабинет**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Используется для запроса информации для следующего CAB-файла.<br/>                                   |
| [**фнфЦижетопенинфо**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Используется для открытия файла и получения даты, времени и атрибутов файла.<br/>                   |
| [**фнфЦижеттемпфиле**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Используется для получения имени временного файла.<br/>                                               |
| [**фнфЦиопен**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Используется для открытия файла в контексте FCI.<br/>                                              |
| [**фнфЦиреад**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Используется для чтения данных из файла.<br/>                                                      |
| [**фнфЦисик**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Используется для перемещения указателя файла в указанное место.<br/>                                |
| [**фнфЦистатус**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Используется для обновления пользователя.<br/>                                                            |
| [**фнфЦиврите**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Используется для записи данных в файл.<br/>                                                       |
| [**ткомпфромлзксвиндов**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Преобразует размер Windows в значение ЛКСЗ ТКОМП для [**фЦиаддфиле**](/windows/desktop/api/Fci/nf-fci-fciaddfile).<br/> |



 

## <a name="fdi-macros"></a>FDI макросы

FDI использует следующие макросы:



| Макрос                              | Описание                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**фналлок**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Используется для выделения памяти в контексте FDI.<br/>                               |
| [**фнклосе**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Используется для закрытия файла в контексте FDI.<br/>                                  |
| [**фнфдинотифи**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Используется для обновления приложения в соответствии с состоянием декодера.<br/>             |
| [**фнфри**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Используется для высвобождения ранее выделенной памяти в контексте FDI.<br/>              |
| [**фнопен**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Используется для открытия файла в контексте FDI.<br/>                                   |
| [**фнреад**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Используется для чтения данных из файла в контексте FDI.<br/>                         |
| [**фнсик**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Используется для перемещения указателя файла в указанное место в контексте FDI.<br/> |
| [**фнврите**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Используется для записи данных в файл в контексте FDI.<br/>                          |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по API CAB-файлов](cabinet-api-reference.md)
</dt> <dt>

[Использование API CAB-файла](using-the-cabinet-api.md)
</dt> </dl>

 

 




