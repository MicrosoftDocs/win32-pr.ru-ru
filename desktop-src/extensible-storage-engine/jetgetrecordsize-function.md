---
description: Дополнительные сведения о функции Жетжетрекордсизе
title: Функция Жетжетрекордсизе
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f42defeefa4d01648d34b971cce994fbebf8f0e8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481300"
---
# <a name="jetgetrecordsize-function"></a>Функция Жетжетрекордсизе


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgetrecordsize-function"></a>Функция Жетжетрекордсизе

Функция **жетжетрекордсизе** извлекает сведения о размере записи из нужного расположения.

**Windows vista: жетжетрекордсизе** появился в Windows Vista.

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Определяет контекст сеанса базы данных, который будет использоваться для вызова API.

*TableID*

Определяет таблицу или курсор, которые будут использоваться для вызова API. Курсор должен быть размещен в записи или иметь подготовленное обновление.

*прексизе*

Указатель на выходной буфер для структуры [JET_RECSIZE](./jet-recsize-structure.md) .

*грбит*

Это одно или несколько из следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Это Извлекает размер записи, которая находится в буфере копирования, подготовленном для обновления. В противном случае <em>tableid</em> или курсор должны быть расположены в записи, и эта запись будет использоваться.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Если этот бит указан, то перед заполнением содержимого <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> не обнуляются, эффективно выполняя сбор статистики по нескольким просмотренным или обновленным записям.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Это приводит к тому, что API пропускает не внутренние значения long. Например, будет использоваться только локальная запись на странице.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Один из запрошенных параметров недопустим или не реализован. Эта ошибка будет возвращена функцией <strong>жетжетрекордсизе</strong> при указании недопустимого <em>грбит</em> .</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, не был инициализирован.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable будет возвращено только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errTermInProgress</p> | <p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Нельзя одновременно использовать один сеанс из нескольких потоков.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable будет возвращено только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Это может произойти, если курсор был размещен неправильно.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Если курсор не был помещен в транзакцию, это может произойти, если другой поток удаляет запись из этого сеанса.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Это может быть возвращено, если передано <strong>значение NULL</strong><em>прексизе</em> .</p> | 



#### <a name="remarks"></a>Комментарии

Размер ключа, накопленного в поле **кбоверхеад** [JET_RECSIZE](./jet-recsize-structure.md), зависит от JET_bitRecordSizeInCopyBuffer. Если этот бит указан, размер ключа, накопленный в поле **кбоверхеад** , является полным размером ключа. Если этот бит не используется, то размер ключа, накопленный, не будет включать размер, сохраненный из-за сжатия префикса ключа.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
