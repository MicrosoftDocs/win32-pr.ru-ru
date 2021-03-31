---
description: Интерфейс Идовнлоадпрогресс определяет следующие свойства.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Свойства Идовнлоадпрогресс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991175"
---
# <a name="idownloadprogress-properties"></a>Свойства Идовнлоадпрогресс

Интерфейс [**идовнлоадпрогресс**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) определяет следующие свойства.



| Свойство                                                                               | Описание                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**куррентупдатебитесдовнлоадед**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | Возвращает строку, которая указывает, сколько данных было передано для файла содержимого или файлов загружаемого обновления в байтах.  |
| [**куррентупдатебитестодовнлоад**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | Возвращает строку, которая определяет объем данных, которые должны быть переданы для файла содержимого или файлов, загружаемых при обновлении, в байтах. |
| [**куррентупдатедовнлоадфасе**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | Возвращает значение перечисления [**довнлоадфасе**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) , указывающее фазу загрузки, которая выполняется в данный момент.          |
| [**куррентупдатеиндекс**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | Возвращает значение индекса, начинающееся с нуля, указывающее обновление, которое загружается в данный момент, когда было выбрано несколько обновлений.             |
| [**куррентупдатеперценткомплете**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | Возвращает оценку процента текущего обновления, которое было загружено.                                                               |
| [**PercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | Возвращает оценку процента всех загруженных обновлений.                                                                 |
| [**TotalBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | Возвращает строку, указывающую общий объем скачанных данных в байтах.                                                        |
| [**тоталбитестодовнлоад**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | Возвращает строку, представляющую оценку общего объема данных, которые будут скачаны в байтах.                                        |



 

 

 



