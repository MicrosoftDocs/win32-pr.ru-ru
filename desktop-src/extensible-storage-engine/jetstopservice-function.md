---
description: Дополнительные сведения о функции Жетстопсервице
title: Функция JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711201"
---
# <a name="jetstopservice-function"></a>Функция JetStopService


_**Применимо к:** Windows | Windows Server_

## <a name="jetstopservice-function"></a>Функция JetStopService

Функция **жетстопсервице** готовит экземпляр к завершению.

**Жетстопсервице** — это устаревший вызов, если разрешен только один экземпляр. В этом случае единственным активным экземпляром является тот, который подготавливается к завершению.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Параметры

У этой функции нет параметров.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

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
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Не ясно, какой экземпляр подготавливается к завершению при использовании <strong>жетстопсервице</strong> в режиме с несколькими экземплярами.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
</tbody>
</table>


Если эта функция выполнена, она подготавливается к будущему завершению. Ниже приведены шаги, предпринимаемые для подготовки к завершению работы.

  - Останавливает оперативную дефрагментацию, если она запущена.

  - Запуск очистки хранилища версий.

  - Уменьшите глубину контрольной точки, начав с очистки «грязных» страниц в диспетчере буферов.

  - Предотвращение будущих вызовов большинства функций для этого экземпляра.

Если эта функция завершается ошибкой, не будет выполнен ни один из шагов подготовки к завершению работы экземпляра, поэтому изменение состояния экземпляра не выполняется.

#### <a name="remarks"></a>Комментарии

Эта функция сокращает работу, которую экземпляр будет выполнять при завершении, но не будет завершать экземпляр. В результате эта функция является просто оптимизацией и не является обязательной для использования. Обратите внимание, что объем работы, выполненной в процессе подготовки, был меньше в Windows 2000 и Windows XP. После выполнения функции вызов функций, которые больше не разрешены, возвратит JET_errClientRequestToStopJetService. Функции, по-прежнему разрешенные после этого вызова: [жетроллбакк](./jetrollback-function.md), [жетклосетабле](./jetclosetable-function.md), [жетендсессион](./jetendsession-function.md), [жетклоседатабасе](./jetclosedatabase-function.md), [жетдетачдатабасе](./jetdetachdatabase-function.md) и [жетресетсессионконтекст](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
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


#### <a name="see-also"></a>См. также:

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
