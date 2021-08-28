---
description: 'Дополнительные сведения: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
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
ms.openlocfilehash: da7acc706017c0346e5a701144d60bcbbfd7cf40
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983797"
---
# <a name="jet_sesid"></a>JET_SESID


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_sesid"></a>JET_SESID

**JET_SESID** тип данных содержит маркер сеанса, используемый для вызова API Jet.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Типы данных

JET_SESID

Для указания недопустимого обработчика сеанса можно использовать **значение NULL** или [JET_sesidNil](./invalid-handle-constants.md) .

### <a name="remarks"></a>Комментарии

Сеанс — это контекст транзакции ядра СУБД. Его можно использовать для начала, фиксации или прерывания транзакций, влияющих на видимость и устойчивость изменений, внесенных в этом или других сеансах.

Транзакцию можно запустить с помощью [жетбегинтрансактион](./jetbegintransaction-function.md). Сеанс можно создать с помощью [жетбегинсессион](./jetbeginsession-function.md). Максимальное число сеансов, которые могут быть созданы за один раз, контролируется [JET_paramMaxSessions](./resource-parameters.md), которые можно настроить с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).

Сеанс явно завершается вызовом [жетендсессион](./jetendsession-function.md) или неявно завершается вызовом [жеттерм](./jetterm-function.md).

Каждый сеанс может использоваться только одним потоком за раз. Кроме того, поведение обработчика по умолчанию заключается в ограничении использования сеанса тем же потоком с момента выполнения первого вызова [жетбегинтрансактион](./jetbegintransaction-function.md) до тех пор, пока не будет произведен соответствующий вызов [жеткоммиттрансактион](./jetcommittransaction-function.md) или [жетроллбакк](./jetrollback-function.md) . Это поведение можно изменить, чтобы удалить это второе ограничение, задав пользовательский контекст сеанса с помощью [жетсетсессионконтекст](./jetsetsessioncontext-function.md) и [жетресетсессионконтекст](./jetresetsessioncontext-function.md).

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_paramMaxSessions](./resource-parameters.md)  
[жетбегинсессион](./jetbeginsession-function.md)  
[жетбегинтрансактион](./jetbegintransaction-function.md)  
[жеткоммиттрансактион](./jetcommittransaction-function.md)  
[жетендсессион](./jetendsession-function.md)  
[жетресетсессионконтекст](./jetresetsessioncontext-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетсетсессионконтекст](./jetsetsessioncontext-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[жеттерм](./jetterm-function.md)
