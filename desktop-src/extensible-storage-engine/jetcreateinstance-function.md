---
description: Дополнительные сведения о функции Жеткреатеинстанце
title: Функция JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713074"
---
# <a name="jetcreateinstance-function"></a>Функция JetCreateInstance


_**Применимо к:** Windows | Windows Server_

## <a name="jetcreateinstance-function"></a>Функция JetCreateInstance

Функция **жеткреатеинстанце** выделяет новый экземпляр ядра СУБД для использования в одном процессе.

**Windows XP: жеткреатеинстанце** появился в Windows XP.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Параметры

*пинстанце*

Выходной буфер, который получает только что созданный экземпляр.

*сзинстанценаме*

Уникальный идентификатор строки для создаваемого экземпляра. Эта строка должна быть уникальной в пределах данного процесса, в котором размещается ядро СУБД.

**Примечание** . Значение NULL обрабатывается как допустимый строковый идентификатор для экземпляра. Только один экземпляр может иметь строковый идентификатор NULL.

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
<td><p>JET_errInstanceNameInUse</p></td>
<td><p>Указанное имя экземпляра уже используется для этого процесса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти для <strong>жеткреатеинстанце</strong> , когда <em>Пинстанце</em> имеет <strong>значение NULL</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Операция завершилась ошибкой, так как ее нельзя использовать, если ядро СУБД работает в режиме одиночного экземпляра (режим совместимости с Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances</p></td>
<td><p>Не удалось создать новый экземпляр, так как достигнуто максимальное число экземпляров. Максимальное число поддерживаемых экземпляров настраивается с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с помощью <em>JET_paramMaxInstances</em>.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении будет выделена новая копия, и будет возвращен идентификатор для него. На этом этапе все системные параметры экземпляра будут иметь значения глобальных системных параметров по умолчанию. После того как экземпляр будет выделен, он должен быть завершен и/или освобожден позже.

В случае сбоя будет возвращена ошибка, представляющая причину сбоя, и ни один экземпляр не будет выделен.

#### <a name="remarks"></a>Комментарии

Экземпляр должен быть инициализирован с помощью вызова [жетинит](./jetinit-function.md) , прежде чем он сможет использоваться любым другим, кроме [жетсетсистемпараметер](./jetsetsystemparameter-function.md).

Экземпляр уничтожается вызовом функции [жеттерм](./jetterm-function.md) , даже если этот экземпляр никогда не был инициализирован с помощью [жетинит](./jetinit-function.md). Максимальное число экземпляров, которые могут быть созданы за один раз, управляется [JET_paramMaxInstances](./resource-parameters.md), которые можно настроить с помощью вызова [жетсетсистемпараметер](./jetsetsystemparameter-function.md). Экземпляр — это единица восстановления для ядра СУБД. Он управляет жизненным циклом всех файлов, используемых для защиты целостности данных в наборе файлов базы данных. Эти файлы включают файл контрольных точек и файлы журнала транзакций.

Если функция выполнена, ядро СУБД автоматически перейдет в режим с несколькими экземплярами как побочный результат этого вызова. Если приложению нужно разрешить только один экземпляр в процессе, то для запуска ядра СУБД в режиме совместимости Windows 2000 следует использовать [жетинит](./jetinit-function.md) .

При наличии *сздисплайнаме* будет использоваться для указания экземпляра в таких местах, как журнал событий, или для других вызывающих объектов, таких как резервные приложения (с помощью таких функций, как [жетжетинстанцеинфо](./jetgetinstanceinfo-function.md) или [жетосснапшотфризе](./jetossnapshotfreeze-function.md)). Если отображаемое имя не указано, вместо него будет использоваться уникальный *сзинстанценаме* , в противном случае будет возвращена пустая строка. Если в обработчике не установлен режим выполнения, после этого вызова он будет установлен в режим с несколькими экземплярами.

Типичная последовательность запуска для процесса, потенциально выполняющего несколько экземпляров Jet, будет выглядеть следующим образом:

  - Вызов [JetCreateInstance2](./jetcreateinstance2-function.md) , который выделит и назначит имя экземпляра.

  - Несколько вызовов [жетсетсистемпараметер](./jetsetsystemparameter-function.md) для этого экземпляра, чтобы задать различные системные параметры. Обратите внимание, что некоторые системные параметры должны быть уникальными для каждого экземпляра (например, [JET_paramSystemPath](./transaction-log-parameters.md) или [JET_paramLogFilePath](./transaction-log-parameters.md)), поэтому, скорее всего, потребуется установить каждый из них.

  - Запустите экземпляр с помощью [жетинит](./jetinit-function.md) или [JetInit2](./jetinit2-function.md). Чтобы завершить и (или) освободить экземпляр, необходимо использовать [жеттерм](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) .

Если это первый экземпляр для запуска, существует ряд дополнительных шагов, которые будут выполнены во время этого вызова для выполнения базовой инициализации и настройки системы. Некоторые из этих шагов могут привести к возникновению конкретных ошибок, начинающихся с JET_errOutOfMemory, а также других (см. ошибки выше).

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista или Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008 или Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>жеткреатеинстанцев</strong> (Юникод) и <strong>жеткреатеинстанцеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[Расширяемые файлы подсистемы хранилища](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[жетенаблемултиинстанце](./jetenablemultiinstance-function.md)  
[жетжетинстанцеинфо](./jetgetinstanceinfo-function.md)  
[жетинит](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[жеттерм](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
