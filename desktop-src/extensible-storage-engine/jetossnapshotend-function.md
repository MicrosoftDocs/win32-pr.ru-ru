---
description: Дополнительные сведения о функции Жетосснапшотенд
title: Функция Жетосснапшотенд
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b57528899b8d78ecee31f6dd54c2ac8decece383
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984437"
---
# <a name="jetossnapshotend-function"></a>Функция Жетосснапшотенд


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetossnapshotend-function"></a>Функция Жетосснапшотенд

Функция **жетосснапшотенд** уведомляет модуль о завершении сеанса моментального снимка.

**Windows vista:****жетосснапшотенд** появился в Windows Vista:.  

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
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
| <p>0</p> | <p>Успешное завершение сеанса моментального снимка.</p> | 
| <p>JET_bitAbortSnapshot</p> | <p>Сеанс моментального снимка прерван.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Один из запрошенных параметров недопустим, используется неправильно или не реализован.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Сеанс моментального снимка уже выполняется. Это не допускается.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Недопустимый идентификатор сеанса моментального снимка.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>Время сеанса моментального снимка истекло до возникновения этого вызова. В результате операции ввода-вывода, возвращенные в нормальный режим до того, как был выполнен этот вызов.</p> | 



Если эта функция завершается, то сеанс моментального снимка будет завершен и будет возобновлено нормальное поведение ядра. Новый сеанс моментального снимка можно запустить позже.

Если эта функция завершается ошибкой, возвращается код возврата JET_errOSSnapshotTimeOut и текущий сеанс моментального снимка завершается, но замораживание IOs в течение периода моментального снимка не учитывается внутренне. Для всех остальных ошибок состояние сеанса моментального снимка не изменится.

#### <a name="remarks"></a>Комментарии

Эта функция вызывается, только если [жетосснапшотсав](./jetossnapshotthaw-function.md) был вызван с JET_bitContinueAfterThaw.

Сеанс моментального снимка должен быть завершен для проверки моментальных снимков и усечения журнала. Записи журнала событий будут созданы для различных этапов создания моментального снимка.

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
[жетосснапшотсав](./jetossnapshotthaw-function.md)
