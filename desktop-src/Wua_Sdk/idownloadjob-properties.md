---
description: Интерфейс Идовнлоаджоб определяет следующие свойства.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Свойства Идовнлоаджоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701647"
---
# <a name="idownloadjob-properties"></a>Свойства Идовнлоаджоб

Интерфейс [**идовнлоаджоб**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) определяет следующие свойства.



| Свойство                                        | Описание                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Возвращает объект состояния, относящегося к вызывающему объекту, который передается в метод [**иупдатедовнлоадер. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Возвращает параметр, указывающий, полностью ли был обработан вызов [**иупдатедовнлоадер. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) . |
| [**Обновления**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Возвращает интерфейс, содержащий доступную только для чтения коллекцию обновлений, указанных в скачивании.                                                  |



 

 

 



