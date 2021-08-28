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
ms.openlocfilehash: 95d74873fabfe27bc9750f074cd656b17e04803e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988086"
---
# <a name="jetbeginexternalbackupinstance-function"></a>Функция Жетбегинекстерналбаккупинстанце


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetbeginexternalbackupinstance-function"></a>Функция Жетбегинекстерналбаккупинстанце

Функция **жетбегинекстерналбаккупинстанце** инициирует внешнюю архивацию, пока ядро и база данных находятся в сети и активны.

**Windows xp: жетбегинекстерналбаккупинстанце** появился в Windows XP.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр базы данных, используемый для этого вызова.

для Windows 2000, вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр. В этом случае подразумевается использование этого одного глобального экземпляра.

для Windows XP и более поздних выпусков вариант API, который не принимает этот параметр, может вызываться только в том случае, если модуль находится в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр. В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.

*грбит*

Группа битов, задающая ноль или более следующих параметров.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Этот флаг является устаревшим. Использование этого бита приведет к возвращению JET_errInvalidgrbit.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Создает добавочное резервное копирование, а не полное резервное копирование. Это означает, что резервное копирование выполняется только для файлов журнала с момента последнего полного или добавочного резервного копирования.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Зарезервировано для последующего использования. определено для Windows XP.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Система может создать коды успеха или сбоя в результате вызова этой функции. полный список ошибок для этого API см. в разделе [коды ошибок расширенных служба хранилища Engine](./extensible-storage-engine-error-codes.md).

См. [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Комментарии

**Жетбегинекстерналбаккупинстанце** — это первая функция в серии функций, которая должна вызываться для успешного выполнения резервного копирования (не на основе VSS). См. также [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) и [жетстопбаккупинстанце](./jetstopbackupinstance-function.md).

Внешнюю резервную копию можно использовать для реализации полных, добавочных или разностных резервных копий.

Резервное копирование будет нечетким, в то время как резервная копия будет соответствовать одному моменту времени в журнале транзакций, но в данный момент нельзя будет контролировать конкретный момент времени.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



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
