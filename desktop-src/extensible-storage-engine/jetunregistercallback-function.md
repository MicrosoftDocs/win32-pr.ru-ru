---
description: Дополнительные сведения о функции Жетунрегистеркаллбакк
title: Функция Жетунрегистеркаллбакк
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87c308f4895eb3e78a35338fe39afb3d775da095
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986497"
---
# <a name="jetunregistercallback-function"></a>Функция Жетунрегистеркаллбакк


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetunregistercallback-function"></a>Функция Жетунрегистеркаллбакк

Функция **жетунрегистеркаллбакк** позволяет приложению настроить ядро СУБД на отмену отправки уведомлений приложению, как ранее было запрошено через [жетрегистеркаллбакк](./jetregistercallback-function.md).

**Windows xp:****жетунрегистеркаллбакк** появился в Windows XP.  

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*кбтип*

Битовая маска, состоящая из причин обратного вызова, которые приложение больше не хочет получать уведомления.

Чтобы создать эту битовую маску, можно просто или совместно использовать допустимые причины обратного вызова из перечисления [JET_CBTYP](./jet-cbtyp.md) .

*хкаллбаккид*

Маркер зарегистрированного обратного вызова, возвращенный [жетрегистеркаллбакк](./jetregistercallback-function.md).

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p><p><strong>Windows XP:</strong>  это возвращаемое значение вводится в Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p><p><strong>Windows XP:</strong>  это возвращаемое значение вводится в Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 



Если эта функция завершилась удачно, указанный обратный вызов будет отменен для заданной причины обратного вызова с таблицей, связанной с данным курсором. Изменение состояния базы данных не выполняется.

Если эта функция завершается с ошибкой, регистрация указанного обратного вызова не будет отменена. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Комментарии

Заданная битовая маска должна точно соответствовать битовой маске, указанной при регистрации обратного вызова. В настоящее время ядро СУБД не поддерживает удаление подмножества этих уведомлений и не возвращает ошибку при выполнении этой попытки.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетрегистеркаллбакк](./jetregistercallback-function.md)  
[жетстопсервице](./jetstopservice-function.md)
