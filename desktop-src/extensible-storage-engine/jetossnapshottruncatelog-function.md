---
description: Дополнительные сведения о функции Жетосснапшоттрункателог
title: Функция Жетосснапшоттрункателог
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da8e76b1c735f6249f1d7e3893acd1db1743b65
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985867"
---
# <a name="jetossnapshottruncatelog-function"></a>Функция Жетосснапшоттрункателог


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetossnapshottruncatelog-function"></a>Функция Жетосснапшоттрункателог

Функция **жетосснапшоттрункателог** включает усечение журнала для всех экземпляров, которые являются частью сеанса моментальных снимков.

**Windows vista:****жетосснапшоттрункателог** появился в Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*снапид*

Идентификатор сеанса моментального снимка.

*грбит*

Параметры для этого вызова. Этот параметр может иметь сочетание следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitAllDatabasesSnapshot</p> | <p>Все базы данных подключены, поэтому подсистема хранилища может вычислять и выполнять усечение журнала.</p> | 
| <p>0 (ноль)</p> | <p>Усечение не выполняется.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Недопустимый параметр <em>грбит</em> .</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Сеанс моментального снимка не находится в состоянии, в котором может произойти усечение. Возможные причины:</p><ul><li><p>вызов выполняется по истечении времени ожидания сеанса моментальных снимков</p></li><li><p>сеанс был указан в качестве моментального снимка копии</p></li></ul> | 



При успешном выполнении файлы журнала для одной или всех экземпляров сеанса моментальных снимков будут обрезаны, если это возможно.

#### <a name="remarks"></a>Комментарии

Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра JET_bitContinueAfterThaw. В противном случае сеанс моментального снимка был бы завершен после вызова [жетосснапшотсав](./jetossnapshotthaw-function.md) .

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[Параметры обработки ошибок](./error-handling-parameters.md)  
[ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[жетосснапшотенд](./jetossnapshotend-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)
