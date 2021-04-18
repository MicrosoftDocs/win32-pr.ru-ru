---
description: ELS поддерживает функции, определенные в следующей таблице.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Расширенные функции лингвистических служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650908"
---
# <a name="extended-linguistic-services-functions"></a>Расширенные функции лингвистических служб

ELS поддерживает функции, определенные в следующей таблице.



| Функция                                                 | Описание                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**маппингкаллбаккпрок**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | Определяемая приложением функция обратного вызова, которая асинхронно обрабатывает данные, созданные функцией **маппингрекогнизетекст** .                 |
| [**маппингдоактион**](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | Заставляет службу ELS выполнить действие после распознавания текста.                                                                |
| [**маппингфрипропертибаг**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | Освобождает память и ресурсы, выделенные во время операции распознавания текста ELS.                                                                 |
| [**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | Освобождает память и ресурсы, выделенные для взаимодействия приложения с одной или несколькими службами ELS.                                            |
| [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | Извлекает список доступных служб, поддерживаемых платформой ELS, вместе со связанной информацией в соответствии с заданным приложением критерием. |
| [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | Вызывает службу ELS для распознавания текста.                                                                                                   |



 

 

 



