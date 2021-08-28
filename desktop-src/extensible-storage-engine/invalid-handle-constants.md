---
description: 'Дополнительные сведения: недопустимые константы Handle'
title: Недопустимые константы Handle
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: 28a52b2fc7a51572cc7bb78ad7631df41438310a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473280"
---
# <a name="invalid-handle-constants"></a>Недопустимые константы Handle


_**Применимо к:** Windows | Windows Сервером_

## <a name="invalid-handle-constants"></a>Недопустимые константы Handle

Следующие константы указывают недопустимые дескрипторы для различных аспектов ESE.


| <p>Константа/значение</p> | <p>Описание</p> | 
|-----------------------|--------------------|
| <p>JET_instanceNil<br />(~ (JET_INSTANCE) 0)</p> | <p>Недопустимый обработчик для экземпляра базы данных.<br /><strong>Windows XP:</strong> появилось в Windows XP.</p> | 
| <p>JET_sesidNil<br />(~ (JET_SESID) 0)</p> | <p>Недопустимый обработчик для идентификатора сеанса.</p> | 
| <p>JET_tableidNil<br />(~ (JET_TABLEID) 0)</p> | <p>Недопустимый обработчик для идентификатора таблицы.</p> | 
| <p>JET_bitNil<br />((JET_GRBIT) 0)</p> | <p>Недопустимый маркер для группы битов.</p> | 
| <p>JET_LSNil<br />(~ (JET_LS) 0)</p> | <p>недопустимый обработчик для локального служба хранилища.</p> | 
| <p>JET_dbidNil<br />((JET_DBID) 0xFFFFFFFF)</p> | <p>Недопустимый обработчик для идентификатора базы данных.</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


