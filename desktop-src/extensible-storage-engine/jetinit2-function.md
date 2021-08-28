---
description: Дополнительные сведения о функции JetInit2
title: Функция JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7874c475dc18beb5d7f6849b9f628ea06cbc32a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470459"
---
# <a name="jetinit2-function"></a>Функция JetInit2


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetinit2-function"></a>Функция JetInit2

Функция **JetInit2** помещает ядро СУБД в состояние, где оно может поддерживать использование файлов базы данных приложением. Подсистема уже должна быть правильно настроена для инициализации с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md). Восстановление после сбоя базы данных выполняется автоматически в рамках процесса инициализации.

**Windows xp:****JetInit2** появился в Windows XP.  

Эта функция является устаревшей. Вместо этого используйте [JetInit3](./jetinit3-function.md) .

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Параметры

*пинстанце*

Экземпляр, используемый для этого вызова.

для Windows 2000 этот параметр игнорируется и всегда должен иметь значение NULL.

для Windows XP и более поздних выпусков использование этого параметра зависит от режима работы ядра. если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь значение null или иметь допустимый выходной буфер, содержащий NULL или JET_instanceNil, который возвращает глобальный экземпляр, созданный в качестве побочного результата инициализации. Этот экземпляр можно передать в любой другой API, который принимает экземпляр. Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть установлен в допустимый входной буфер, содержащий экземпляр, возвращенный [жеткреатеинстанце](./jetcreateinstance-function.md) , который инициализируется.

*грбит*

Группа битов, задающая ноль или более следующих параметров.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Зарезервировано для последующего использования.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Зарезервировано для последующего использования.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Этот параметр позволяет пользователю выполнять восстановление на наборе файлов журнала без всех существующих баз данных, подключенных к одной точке набора журналов.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Выполните восстановление, но остановите на этапе отката. Это позволяет копировать и применять дополнительные журналы транзакций.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>При успешном обратимом восстановлении усечение файлов журнала.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Отсутствует запись схемы базы данных по умолчанию в то же расположение.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Игнорировать журналы, потерянные с конца потока журнала.</p><p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> введен в Windows 7.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


#### <a name="remarks"></a>Комментарии

Экземпляр должен быть инициализирован с помощью вызова **JetInit2** , прежде чем он сможет использоваться любым другим, кроме [жетсетсистемпараметер](./jetsetsystemparameter-function.md).

Экземпляр уничтожается вызовом функции [жеттерм](./jetterm-function.md) , даже если этот экземпляр никогда не был инициализирован с помощью [жетинит](./jetinit-function.md). Экземпляр — это единица восстановления для ядра СУБД. Он управляет жизненным циклом всех файлов, используемых для защиты целостности данных в наборе файлов базы данных. Эти файлы включают файл контрольных точек и файлы журнала транзакций.

Если восстановление выполняется на наборе журналов, для которых не все базы данных (возвращающие ошибку JET_errAttachedDatabaseMismatch при нормальных обстоятельствах), и клиент хочет, чтобы продолжение восстановления, несмотря на отсутствие баз данных, JET_ Битреплайигноремиссингдб используется для продолжения восстановления доступных баз данных.

Дополнительные сведения см. в разделе "Примечания" в [жетинит](./jetinit-function.md) .

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[расширяемые файлы служба хранилища Engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетинит](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[Параметры ресурсов](./resource-parameters.md)
