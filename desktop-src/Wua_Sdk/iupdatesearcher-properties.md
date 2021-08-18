---
description: Интерфейс Иупдатесеарчер определяет следующие свойства.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Свойства Иупдатесеарчер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dc3af2635fff4260a44261333b23cbfcf1661793ad613f08bb288db452b93d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130436"
---
# <a name="iupdatesearcher-properties"></a>Свойства Иупдатесеарчер

Интерфейс [**иупдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) определяет следующие свойства.



| Свойство                                                                                           | Описание                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**канаутоматикаллюпградесервице**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | возвращает и задает логическое значение, указывающее, приводит ли будущие вызовы методов [**бегинсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) и [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) к автоматическому обновлению до Центр обновления Windows Agent (WUA). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Определяет текущее клиентское приложение.                                                                                                                                                                                                   |
| [**инклудепотентиаллисуперседедупдатес**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Возвращает и задает логическое значение, указывающее, содержат ли результаты поиска обновления, заменяемые другими обновлениями в результатах поиска.                                                                                          |
| [**Миграция по сети**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Возвращает и задает логическое значение, указывающее, переходит ли [**упдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) в оперативный режим для поиска обновлений.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | возвращает и задает сайт для поиска, если сайт для поиска не является Центр обновления Windows сайтом.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Возвращает и задает значение [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) , указывающее сервер для поиска обновлений.                                                                                                                            |




 

 

 



