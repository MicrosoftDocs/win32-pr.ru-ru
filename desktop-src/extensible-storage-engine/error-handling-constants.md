---
description: 'Дополнительные сведения: обработка ошибок констант'
title: Константы обработки ошибок
TOCTitle: Error Handling Constants
ms:assetid: 5a1f9438-2d36-483e-9820-d0de30ee5e01
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269258(v=EXCHG.10)
ms:contentKeyID: 32765560
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
ms.openlocfilehash: 4480b54277c1586ca05d4a5db2ca6fdb9e045055
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987637"
---
# <a name="error-handling-constants"></a>Константы обработки ошибок


_**Применимо к:** Windows | Windows Сервером_

## <a name="error-handling-constants"></a>Константы обработки ошибок

Для задания диапазона [JET_paramExceptionAction](./error-handling-parameters.md) системных параметров используются следующие константы.


| <p>Константа/значение</p> | <p>Описание</p> | 
|-----------------------|--------------------|
| <p>JET_ExceptionMsgBox<br />0x0001</p> | <p>Отображает окно сообщения при возникновении исключения.</p> | 
| <p>JET_ExceptionNone<br />0x0002</p> | <p>Не выполняет никаких действий при возникновении исключения.</p> | 



### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[Параметры обработки ошибок](./error-handling-parameters.md)
