---
description: Дополнительные сведения о функции Жетжетсессионпараметер
title: Функция Жетжетсессионпараметер
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 183169f8356a664b450e74534558286607fed62c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984777"
---
# <a name="jetgetsessionparameter-function"></a>Функция Жетжетсессионпараметер


_**Применимо к:** Windows | Windows Сервером_

Функция **жетжетсессионпараметер** считывает параметр сеанса для данного сеанса.

функция **жетжетсессионпараметер** была введена в операционной системе Windows 8.

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

Если этот параметр указан, то указанный экземпляр игнорируется, и будет использоваться экземпляр, связанный с сеансом.

*сеспарамид*

ИДЕНТИФИКАТОР устанавливаемого параметра сеанса.

*пвпарам*

Данные в этом параметре сеанса.

*кбпараммакс*

Максимальный размер набора данных в этом параметре сеанса.

*пкбпарамактуал*

Фактический размер набора данных в этом параметре сеанса.

### <a name="return-value"></a>Возвращаемое значение

В случае успеха выходной буфер, соответствующий запрошенному параметру сеанса, будет установлен в значение этого параметра сеанса.

В случае сбоя состояние выходных буферов будет не определено.

#### <a name="remarks"></a>Комментарии

Параметр Session используется в течение времени существования сеанса или до тех пор, пока значение не будет сброшено.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>Требуется Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Требуется Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также раздел

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетинит](./jetinit-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
