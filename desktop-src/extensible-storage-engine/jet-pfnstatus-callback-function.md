---
description: 'Дополнительные сведения: функция обратного вызова JET_PFNSTATUS'
title: Функция обратного вызова JET_PFNSTATUS
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: d10de8491379a3e19217bcdb4a28f3546ebc009f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482920"
---
# <a name="jet_pfnstatus-callback-function"></a>Функция обратного вызова JET_PFNSTATUS


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_pfnstatus-callback-function"></a>Функция обратного вызова JET_PFNSTATUS

Функция обратного вызова **JET_PFNSTATUS** получает сведения о ходе выполнения длительных операций, таких как дефрагментация, операции резервного копирования или восстановления. Во время таких операций ядро СУБД вызывает эту функцию обратного вызова, чтобы обеспечить обновление хода выполнения операции.

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс типа [JET_SESID](./jet-sesid.md) , с которым была вызвана долго выполняющаяся функция.

*Network*

Тип операции, указанный в [JET_SNP](./jet-snp.md). К типам операций относятся исправление, сжатие, восстановление, резервное копирование, обновление, очистка и обновление формата записи.

*снт*

Состояние операции. Типы состояния включают "начало", "выполняется", "завершение" или "сбой". Состояние будет указано с помощью третьего параметра типа [JET_SNT](./jet-snt.md).

*PV*

Необязательный указатель на структуру типа [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Возвращаемое значение

эта функция возвращает [JET_ERR](./jet-err.md) datatype с одним из [кодов ошибок расширяемого механизма служба хранилища](./extensible-storage-engine-error-codes.md). дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).

При успешном выполнении операция, выдала ответный вызов, может продолжать работу в обычном режиме. В некоторых случаях обратный вызов может возвращать предупреждение, которое влияет на эту операцию.

В случае сбоя операция, выдала ответный вызов, может продолжаться обычным образом или не может завершиться ошибкой.

### <a name="remarks"></a>Комментарии

Эта функция обратного вызова будет использоваться в уведомлении о ходе выполнения, в которой структура будет указывать текущее состояние хода выполнения. Обратите внимание, что функция обратного вызова может вызываться несколько раз для выполнения операции.

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[коды ошибок расширенного механизма служба хранилища](./extensible-storage-engine-error-codes.md)  
[ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
