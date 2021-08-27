---
description: Дополнительные сведения о функции Жетосснапшотпрепаре
title: Функция JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 010cafd19ffde09b3083dd3cb6e6a69fa2268f11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470331"
---
# <a name="jetossnapshotprepare-function"></a>Функция JetOSSnapshotPrepare


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetossnapshotprepare-function"></a>Функция JetOSSnapshotPrepare

Функция **жетосснапшотпрепаре** начинает подготовку сеанса моментального снимка. Сеанс моментальных снимков — это короткий интервал времени, в течение которого модуль не выполняет никаких операций записи с диска IOs на диск, чтобы подсистема могла участвовать в сеансе моментальных снимков тома (при использовании модуля записи моментальных снимков).

**Windows xp:****жетосснапшотпрепаре** появился в Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*пснапид*

Идентификатор сеанса моментального снимка, который необходимо запустить.

*грбит*

Параметры для этого вызова. Этот параметр может иметь сочетание следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>0</p> | <p>Стандартный моментальный снимок.</p> | 
| <p>JET_bitIncrementalSnapshot</p> | <p>Будут предприняты только файлы журналов.</p> | 
| <p>JET_bitCopySnapshot</p> | <p>Моментальный снимок копии (обычная или добавочная) без усечения журнала.</p> | 
| <p>JET_bitContinueAfterThaw</p> | <p>Сеанс моментального снимка происходит после <a href="gg269229(v=exchg.10).md">жетосснапшотсав</a> и требует вызова функции <a href="gg294136(v=exchg.10).md">жетосснапшотенд</a> .</p> | 
| <p>JET_bitExplicitPrepare</p> | <p>Ни один экземпляр не будет подготовлен по умолчанию.</p><p><strong>Windows 7:</strong>  JET_bitExplicitPrepare представлен в Windows 7.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Указатель идентификатора моментального снимка имеет значение NULL, или параметр <em>грбит</em> является недопустимым.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Сеанс моментальных снимков уже выполняется, и в данный момент операция не может иметь более одного сеанса моментального снимка.</p> | 



Если эта функция завершится с ошибкой, сеанс моментального снимка можно будет запустить в любое время с фазы замораживания ввода-вывода. Идентификатор сеанса будет возвращен и должен использоваться в последующих вызовах для сеанса моментального снимка.

Выполняющиеся экземпляры подсистемы теперь будут рассматриваться как часть сеанса моментального снимка.

**Windows Vista:**  Чтобы указать другое подмножество экземпляров, можно вызвать [жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md) .

Стандартный вызов последовательности API: **жетосснапшотпрепаре**, при необходимости за одним или несколькими вызовами [жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md), после которого следует [жетосснапшотфризе](./jetossnapshotfreeze-function.md). После запуска замораживания его можно завершить с помощью [жетосснапшотсав](./jetossnapshotthaw-function.md). В любое время после подготовки сеанс моментального снимка может внезапно завершиться с помощью [жетосснапшотаборт](./jetossnapshotabort-function.md).

Если после [жетосснапшотсав](./jetossnapshotthaw-function.md)указан JET_bitContinueAfterThaw, то сеанс моментального снимка останется (хотя операция ввода-вывода будет возобновлена). При этом будет включена проверка моментального снимка и, при необходимости, будет включено усечение журнала с помощью [жетосснапшоттрункателог](./jetossnapshottruncatelog-function.md) и потребуется вызов [жетосснапшотенд](./jetossnapshotend-function.md).

Если эта функция завершается неудачно, изменение состояния модуля не происходит.

#### <a name="remarks"></a>Комментарии

Записи журнала событий будут созданы для различных этапов создания моментального снимка.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[жетосснапшотаборт](./jetossnapshotabort-function.md)  
[жетосснапшотенд](./jetossnapshotend-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)  
[жетосснапшоттрункателог](./jetossnapshottruncatelog-function.md)
