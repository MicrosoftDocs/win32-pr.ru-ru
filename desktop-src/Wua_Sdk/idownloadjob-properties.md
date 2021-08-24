---
description: Интерфейс Идовнлоаджоб определяет следующие свойства.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Свойства Идовнлоаджоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cdd4f95a14df215017f9fd628497d15c6c7410e4a82cbfb53c076b2112899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049345"
---
# <a name="idownloadjob-properties"></a>Свойства Идовнлоаджоб

Интерфейс [**идовнлоаджоб**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) определяет следующие свойства.



| Свойство                                        | Описание                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Возвращает объект состояния, относящегося к вызывающему объекту, который передается в метод [**иупдатедовнлоадер. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Возвращает параметр, указывающий, полностью ли был обработан вызов [**иупдатедовнлоадер. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) . |
| [**Обновляем**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Возвращает интерфейс, содержащий доступную только для чтения коллекцию обновлений, указанных в скачивании.                                                  |



 

 

 



