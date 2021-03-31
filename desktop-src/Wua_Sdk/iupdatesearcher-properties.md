---
description: Интерфейс Иупдатесеарчер определяет следующие свойства.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Свойства Иупдатесеарчер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2021
ms.locfileid: "104354015"
---
# <a name="iupdatesearcher-properties"></a>Свойства Иупдатесеарчер

Интерфейс [**иупдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) определяет следующие свойства.



| Свойство                                                                                           | Описание                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**канаутоматикаллюпградесервице**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Возвращает и задает логическое значение, указывающее, приводит ли будущие вызовы методов [**бегинсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) и [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) к автоматическому обновлению до центр обновления Windows Agent (WUA). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Определяет текущее клиентское приложение.                                                                                                                                                                                                   |
| [**инклудепотентиаллисуперседедупдатес**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Возвращает и задает логическое значение, указывающее, содержат ли результаты поиска обновления, заменяемые другими обновлениями в результатах поиска.                                                                                          |
| [**Миграция по сети**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Возвращает и задает логическое значение, указывающее, переходит ли [**упдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) в оперативный режим для поиска обновлений.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Возвращает и задает сайт для поиска, если сайт для поиска не является Центр обновления Windows сайтом.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Возвращает и задает значение [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) , указывающее сервер для поиска обновлений.                                                                                                                            |




 

 

 



