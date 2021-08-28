---
description: Дополнительные сведения о функции JetStopServiceInstance2
title: Функция JetStopServiceInstance2
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b5446306bd4035c68f33db2966b1cfadd0b6d82
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987237"
---
# <a name="jetstopserviceinstance2-function"></a>Функция JetStopServiceInstance2


_**Применимо к:** Windows | Windows Сервером_

Функция **JetStopServiceInstance2** готовит экземпляр перед приостановкой и готовит экземпляр после возобновления. приостановка и возобновление являются состояниями выполнения модели жизненного цикла приложения для магазина Windows.

Функция **JetStopServiceInstance2** была введена в Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Параметры

*вхождение*

Целевой экземпляр. Тип данных **JET_INSTANCE** является обработчиком экземпляра базы данных, который используется для вызова API Jet. Этот маркер получается при создании экземпляра базы данных путем вызова функций [жеткреатеинстанце](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [жетинит](./jetinit-function.md)или [JetInit2](./jetinit2-function.md) .

*грбит*

Группа битов, задающая одно или несколько значений, перечисленных и определенных в следующей таблице.


| <p>Применение</p> | <p>Описание</p> | 
|--------------|--------------------|
| <p>JET_bitStopServiceAll</p> | <p>останавливает все службы расширенного обработчика служба хранилища (ESE) для указанного экземпляра.</p> | 
| <p>JET_bitStopServiceBackgroundUserTasks</p> | <p>Останавливает Перезапускаемые клиентские задачи фонового обслуживания (например, дефрагментацию дерева B +).</p> | 
| <p>JET_bitStopServiceQuiesceCaches</p> | <p>Куиесцес все "грязные" кэши на диск. Это значение является асинхронным и может быть отменено.</p> | 
| <p>JET_bitStopServiceResume</p> | <p>Возобновляет ранее выданные операции выхода из эксплуатации; то есть он перезапускает службу. Это значение можно сочетать с параметром <em>грбитс</em> , чтобы возобновить работу конкретных служб, или с JET_bitStopServiceAll, чтобы возобновить работу всех ранее остановленных служб. Этот бит можно использовать только для возобновления Стопсервицебаккграундусертаскс и JET_bitStopServiceQuiesceCaches. Если ранее было вызвано с JET_bitStopServiceAll, попытка использовать JET_bitStopServiceResume завершится ошибкой. Если второй шаг возобновления не вызывается, это приведет к снижению производительности приложения. В этом случае контрольная точка остается в нулевом виде.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 



#### <a name="remarks"></a>Комментарии

Эта функция позволяет приложению JET перевести кэш базы данных в состояние чистого или почти чистого состояния (при простом вводе-выпуске операционной системы), например, если приложение должно быть завершено, восстановление было бы быстрым. Этот подход предпочтительнее, чем завершение работы с JET, путем вызова функций [жеттерм](./jetterm-function.md) или [жетдетачдатабасе](./jetdetachdatabase-function.md) , чтобы в более распространенном сценарии приложение было просто неприостановленным, а позднее приложение получило весь кэш и готово к работе как можно скорее.

Если эта функция выполнена, она подготавливает кэш базы данных для приближающейся приостановки. Эта функция очереди работает в фоновом рабочем потоке и немедленно возвращает вызывающему объекту. Функция должна вызываться на основе PLM Висибилитинотице, а не вызывать из обработчика событий приостановки приложения, чтобы гарантировать, что у JET есть время на очистку грязных буферов перед тем, как PLM приостанавливает работу или завершает процесс. На внутреннем уровне JET запускает немедленную отправку обслуживания контрольных точек при изменении конфигурации (обновление контрольной точки или новый бит замораживания кэша). Дополнительные сведения о событиях Висибилитинотице см. в разделе [класс висибилитичанжедевентаргс](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Эта функция должна вызываться дважды. Он вызывается после того, как приложение получает уведомление о приостановке от операционной системы, но до того, как приложение будет приостановлено. Затем он вызывается снова после того, как операционная система возобновит работу приложения. Пример:

При вызове для приостановки: JET_ERR JET_API JetStopServiceInstance2 (экземпляр, JET_bitStopServiceQuiesceCaches);

При возобновлении: JET_ERR JET_API JetStopServiceInstance2 (экземпляр, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>Требуется Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Требуется Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также раздел

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетдетачдатабасе](./jetdetachdatabase-function.md)  
[жетендсессион](./jetendsession-function.md)  
[жетресетсессионконтекст](./jetresetsessioncontext-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жеттерм](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
