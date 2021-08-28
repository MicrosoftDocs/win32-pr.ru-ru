---
description: Дополнительные сведения о функции Жетосснапшоттрункателогинстанце
title: Функция Жетосснапшоттрункателогинстанце
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0986633a450052431dfcef1426488dddc0417d33
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988447"
---
# <a name="jetossnapshottruncateloginstance-function"></a>Функция Жетосснапшоттрункателогинстанце


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetossnapshottruncateloginstance-function"></a>Функция Жетосснапшоттрункателогинстанце

Функция **жетосснапшоттрункателогинстанце** усекает журнал для указанного экземпляра во время сеанса моментального снимка.

**Windows vista:****жетосснапшоттрункателогинстанце** появился в Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*снапид*

Идентификатор сеанса моментального снимка.

*вхождение*

Экземпляр, который будет использоваться для этого вызова.

*грбит*

Параметры для этого вызова. Этот параметр может иметь сочетание следующих значений.

*грбит* может иметь одно из следующих значений:


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
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Сеанс моментального снимка не находится в состоянии, в котором может произойти усечение. Возможные причины:</p><ul><li><p>Вызов завершается после истечения времени ожидания сеанса моментального снимка.</p></li><li><p>Сеанс был указан в качестве моментального снимка копии.</p></li></ul> | 



Если эта функция выполнена, файлы журнала для одного или всех экземпляров, которые являются частью сеанса моментального снимка, будут обрезаны, если это возможно.

#### <a name="remarks"></a>Комментарии

Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра JET_bitContinueAfterThaw. В противном случае сеанс моментального снимка завершается после вызова [жетосснапшотсав](./jetossnapshotthaw-function.md).

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
