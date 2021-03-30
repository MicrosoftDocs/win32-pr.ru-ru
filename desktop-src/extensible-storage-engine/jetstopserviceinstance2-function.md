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
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810360"
---
# <a name="jetstopserviceinstance2-function"></a>Функция JetStopServiceInstance2


_**Применимо к:** Windows | Windows Server_

Функция **JetStopServiceInstance2** готовит экземпляр перед приостановкой и готовит экземпляр после возобновления. Приостановка и возобновление являются состояниями выполнения модели жизненного цикла приложения Магазина Windows.

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitStopServiceAll</p></td>
<td><p>Останавливает все службы расширенного подсистемы хранилища (ESE) для указанного экземпляра.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceBackgroundUserTasks</p></td>
<td><p>Останавливает Перезапускаемые клиентские задачи фонового обслуживания (например, дефрагментацию дерева B +).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitStopServiceQuiesceCaches</p></td>
<td><p>Куиесцес все "грязные" кэши на диск. Это значение является асинхронным и может быть отменено.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceResume</p></td>
<td><p>Возобновляет ранее выданные операции выхода из эксплуатации; то есть он перезапускает службу. Это значение можно сочетать с параметром <em>грбитс</em> , чтобы возобновить работу конкретных служб, или с JET_bitStopServiceAll, чтобы возобновить работу всех ранее остановленных служб. Этот бит можно использовать только для возобновления Стопсервицебаккграундусертаскс и JET_bitStopServiceQuiesceCaches. Если ранее было вызвано с JET_bitStopServiceAll, попытка использовать JET_bitStopServiceResume завершится ошибкой. Если второй шаг возобновления не вызывается, это приведет к снижению производительности приложения. В этом случае контрольная точка остается в нулевом виде.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Эта функция позволяет приложению JET перевести кэш базы данных в состояние чистого или почти чистого состояния (при простом вводе-выпуске операционной системы), например, если приложение должно быть завершено, восстановление было бы быстрым. Этот подход предпочтительнее, чем завершение работы с JET, путем вызова функций [жеттерм](./jetterm-function.md) или [жетдетачдатабасе](./jetdetachdatabase-function.md) , чтобы в более распространенном сценарии приложение было просто неприостановленным, а позднее приложение получило весь кэш и готово к работе как можно скорее.

Если эта функция выполнена, она подготавливает кэш базы данных для приближающейся приостановки. Эта функция очереди работает в фоновом рабочем потоке и немедленно возвращает вызывающему объекту. Функция должна вызываться на основе PLM Висибилитинотице, а не вызывать из обработчика событий приостановки приложения, чтобы гарантировать, что у JET есть время на очистку грязных буферов перед тем, как PLM приостанавливает работу или завершает процесс. На внутреннем уровне JET запускает немедленную отправку обслуживания контрольных точек при изменении конфигурации (обновление контрольной точки или новый бит замораживания кэша). Дополнительные сведения о событиях Висибилитинотице см. в разделе [класс висибилитичанжедевентаргс](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Эта функция должна вызываться дважды. Он вызывается после того, как приложение получает уведомление о приостановке от операционной системы, но до того, как приложение будет приостановлено. Затем он вызывается снова после того, как операционная система возобновит работу приложения. Пример:

При вызове для приостановки: JET_ERR JET_API JetStopServiceInstance2 (экземпляр, JET_bitStopServiceQuiesceCaches);

При возобновлении: JET_ERR JET_API JetStopServiceInstance2 (экземпляр, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
</tbody>
</table>


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
