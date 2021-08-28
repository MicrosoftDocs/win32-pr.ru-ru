---
description: Дополнительные сведения о функции JetGetRecordSize2
title: Функция JetGetRecordSize2
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68c503192f0be157a59e8e3b32c817231f35e25c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478300"
---
# <a name="jetgetrecordsize2-function"></a>Функция JetGetRecordSize2


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgetrecordsize2-function"></a>Функция JetGetRecordSize2

Функция **JetGetRecordSize2** извлекает сведения о размере записи из нужного расположения.

**Windows 7: JetGetRecordSize2** появился в операционной системе Windows 7.

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Определяет контекст сеанса базы данных, который будет использоваться для вызова API.

*TableID*

Определяет таблицу или курсор, которые будут использоваться для вызова API. Курсор должен быть размещен в записи или иметь подготовленное обновление.

*прексизе*

Указатель на выходной буфер для структуры [JET_RECSIZE2](./jet-recsize2-structure.md) .

*грбит*

Это одно или несколько из следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Это Извлекает размер записи, которая находится в буфере копирования, подготовленном для обновления. В противном случае <em>tableid</em> или курсор должны быть расположены в записи, и эта запись будет использоваться.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Если этот бит указан, то перед заполнением содержимого <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> не обнуляются, эффективно выполняя сбор статистики по нескольким просмотренным или обновленным записям.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Это приводит к тому, что API пропускает не внутренние значения long. Например, будет использоваться только локальная запись на странице.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Один из запрошенных параметров недопустим или не реализован. Эта ошибка будет возвращена функцией <strong>JetGetRecordSize2</strong> при указании недопустимого <em>грбит</em> .</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, не был инициализирован.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p><p><strong>Windows XP:</strong> JET_errInstanceUnavailable будет возвращена только операционной системой Windows XP и более поздними версиями Windows.</p> | 
| <p>JET_errTermInProgress</p> | <p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Нельзя использовать один сеанс для нескольких потоков одновременно.</p><p><strong>Windows XP:</strong> JET_errInstanceUnavailable будут возвращаться только Windows XP и более поздних версий Windows.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Это может произойти, если курсор был размещен неправильно.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Если курсор не был помещен в транзакцию, это может произойти, если другой поток удаляет запись из этого сеанса.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Это может быть возвращено, если передано <strong>значение NULL</strong><em>прексизе</em> .</p> | 



#### <a name="remarks"></a>Комментарии

Размер ключа, накопленного в поле **кбоверхеад** [JET_RECSIZE2](./jet-recsize2-structure.md), зависит от JET_bitRecordSizeInCopyBuffer. Если этот бит указан, размер ключа, накопленный в поле **кбоверхеад** , является полным размером ключа. Если этот бит не используется, размер ключа, накопленный, не будет включать размер, сохраненный из-за сжатия префикса ключа.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
