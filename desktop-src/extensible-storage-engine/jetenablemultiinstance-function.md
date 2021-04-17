---
description: Дополнительные сведения о функции Жетенаблемултиинстанце
title: Функция Жетенаблемултиинстанце
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693779"
---
# <a name="jetenablemultiinstance-function"></a>Функция Жетенаблемултиинстанце


_**Применимо к:** Windows | Windows Server_

## <a name="jetenablemultiinstance-function"></a>Функция Жетенаблемултиинстанце

Функция **жетенаблемултиинстанце** настраивает ядро СУБД для использования с несколькими экземплярами в одном процессе. Необязательный массив глобальных системных параметров доступен для первого вызывающего объекта, что позволяет изменять режим с несколькими экземплярами.

**Windows XP: жетенаблемултиинстанце** появился в Windows XP.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Параметры

*псетсиспарам*

Массив глобальных системных параметров, который задается только в том случае, если обработчик переходит в режим с несколькими экземплярами в результате этого вызова. Если *ксетсиспарам* равен нулю, *псетсиспарам* игнорируется.

*ксетсиспарам*

Число элементов для массива глобальных параметров, которые задаются только в том случае, если обработчик переходит в режим с несколькими экземплярами в результате этого вызова. Если *ксетсиспарам* равен нулю, *псетсиспарам* игнорируется.

*пксетсукцеед*

Указатель на число глобальных системных параметров, которые были успешно настроены в результате этого вызова.

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
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Указанные параметры индекса кортежа не допускаются. Эта ошибка может возвращаться <strong>жетенаблемултиинстанце</strong> только при задании недопустимых значений <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>или <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> .</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Указан недопустимый путь к файловой системе. Эта ошибка может возвращаться <strong>жетенаблемултиинстанце</strong> только при задании системных параметров, представляющих пути файловой системы. Например, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> может возвращать эту ошибку.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Операция завершилась ошибкой, так как она недопустима, если ядро СУБД работает в режиме одиночного экземпляра (режим совместимости с Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemParamsAlreadySet</p></td>
<td><p>Сбой <strong>жетенаблемултиинстанце</strong> , так как модуль уже находится в режиме с несколькими экземплярами.</p>
<p><strong>Примечание  </strong> . Это произойдет, даже если системные параметры не указаны.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершится с ошибкой, ядро СУБД будет настроено для работы в режиме с несколькими экземплярами. Для этого механизма также успешно настроен необязательный список глобальных параметров системы.

Если эта функция завершается ошибкой, ядро СУБД остается в текущем режиме. Если *пксетсукцеед* не равно нулю, то это число системных параметров останется установленным.

#### <a name="remarks"></a>Комментарии

Эта функция должна использоваться, только если приложение должно настроить заданный набор системных параметров атомарно при настройке ядра СУБД для использования в сценарии с несколькими пользователями в одном процессе. Если доступен другой метод синхронизации, предпочтительнее вызывать [жеткреатеинстанце](./jetcreateinstance-function.md) и [жетсетсистемпараметер](./jetsetsystemparameter-function.md) отдельно.

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
<td><p>Реализуется как <strong>жетенаблемултиинстанцев</strong> (Юникод) и <strong>жетенаблемултиинстанцеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетинит](./jetinit-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)
