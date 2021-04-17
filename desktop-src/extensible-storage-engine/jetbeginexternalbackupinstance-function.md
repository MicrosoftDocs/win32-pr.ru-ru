---
description: Дополнительные сведения о функции Жетбегинекстерналбаккупинстанце
title: Функция Жетбегинекстерналбаккупинстанце
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496935"
---
# <a name="jetbeginexternalbackupinstance-function"></a>Функция Жетбегинекстерналбаккупинстанце


_**Применимо к:** Windows | Windows Server_

## <a name="jetbeginexternalbackupinstance-function"></a>Функция Жетбегинекстерналбаккупинстанце

Функция **жетбегинекстерналбаккупинстанце** инициирует внешнюю архивацию, пока ядро и база данных находятся в сети и активны.

**Windows XP: жетбегинекстерналбаккупинстанце** появился в Windows XP.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр базы данных, используемый для этого вызова.

Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр. В этом случае подразумевается использование этого одного глобального экземпляра.

Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр. В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.

*грбит*

Группа битов, задающая ноль или более следующих параметров.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Этот флаг является устаревшим. Использование этого бита приведет к возвращению JET_errInvalidgrbit.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Создает добавочное резервное копирование, а не полное резервное копирование. Это означает, что резервное копирование выполняется только для файлов журнала с момента последнего полного или добавочного резервного копирования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Зарезервировано для последующего использования. Определено для Windows XP.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Система может создать коды успеха или сбоя в результате вызова этой функции. Полный список ошибок для этого API см. в разделе [расширенные коды ошибок подсистемы хранилища](./extensible-storage-engine-error-codes.md).

См. [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Комментарии

**Жетбегинекстерналбаккупинстанце** — это первая функция в серии функций, которая должна вызываться для успешного выполнения резервного копирования (не на основе VSS). См. также [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) и [жетстопбаккупинстанце](./jetstopbackupinstance-function.md).

Внешнюю резервную копию можно использовать для реализации полных, добавочных или разностных резервных копий.

Резервное копирование будет нечетким, в то время как резервная копия будет соответствовать одному моменту времени в журнале транзакций, но в данный момент нельзя будет контролировать конкретный момент времени.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)  
[жетклосефиле](./jetclosefile-function.md)  
[жетендекстерналбаккуп](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[жетжетаттачинфо](./jetgetattachinfo-function.md)  
[жетжетлогинфо](./jetgetloginfo-function.md)  
[жетопенфиле](./jetopenfile-function.md)  
[жетреадфиле](./jetreadfile-function.md)  
[жетстопбаккуп](./jetstopbackup-function.md)  
[жеттрункателог](./jettruncatelog-function.md)
