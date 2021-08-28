---
description: 'Дополнительные сведения: константы ведения журнала событий'
title: Константы ведения журнала событий
TOCTitle: Event Logging Constants
ms:assetid: d24603a9-a9be-4700-bc20-4e3f0661e741
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294101(v=EXCHG.10)
ms:contentKeyID: 32765716
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 054c1a62d4a5c6b6203110de47efadae3920a90c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468391"
---
# <a name="event-logging-constants"></a>Константы ведения журнала событий


_**Применимо к:** Windows | Windows Сервером_

## <a name="event-logging-constants"></a>Константы ведения журнала событий

Следующие константы указывают уровень детализации для сообщений журнала событий для системного параметра [JET_ParamEventLoggingLevel](./event-log-parameters.md) .


| <p>Константа/значение</p> | <p>Описание</p> | 
|-----------------------|--------------------|
| <p>JET_EventLoggingDisable<br />0</p> | <p>Отключает ведение журнала событий.</p> | 
| <p>JET_EventLoggingLevelMax<br />100</p> | <p>Задает максимальный уровень, используемый для журналов событий, который в настоящее время 100 символов.</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[Параметры журнала событий](./event-log-parameters.md)
