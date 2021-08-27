---
description: Дополнительные сведения о функции JetEndExternalBackupInstance2
title: Функция JetEndExternalBackupInstance2
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4235736d9933a510922e5fcc4ffc72c27cd0037
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477620"
---
# <a name="jetendexternalbackupinstance2-function"></a>Функция JetEndExternalBackupInstance2


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetendexternalbackupinstance2-function"></a>Функция JetEndExternalBackupInstance2

Функция **JetEndExternalBackupInstance2** завершает внешний сеанс резервного копирования. Этот API является последним в серии API-интерфейсов, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).

**Windows xp: JetEndExternalBackupInstance2** появился в Windows XP.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр, используемый для этого вызова.

**Windows 2000:** для Windows 2000, вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр. В этом случае подразумевается использование этого одного глобального экземпляра.

**Windows XP:** для Windows XP и более поздних выпусков вариант API, который не принимает этот параметр, может вызываться только в том случае, если модуль находится в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр. В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.

*грбит*

Группа битов, которая задает ноль или более следующих параметров.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitBackupEndAbort<br />0x0002</p> | <p>Клиентское приложение прерывает резервное копирование.</p> | 
| <p>JET_bitBackupEndNormal<br />0x0001</p> | <p>Клиентское приложение полностью завершило резервное копирование и завершается нормально.</p> | 
| <p>JET_bitBackupTruncateDone<br />0x0100</p> | <p><strong>Windows Vista:</strong> JET_bitBackupTruncateDone введены в Windows Vista.</p><p>Подсистема может пометить заголовки базы данных соответствующим образом (например, завершить полное резервное копирование), даже если вызов truncate не был завершен.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errBackupAbortByCaller</p> | <p><strong>Windows XP:</strong> это возвращаемое значение вводится в Windows XP.</p><p>Вызывающий объект прервал резервную копию в середине последовательности резервного копирования, не указывая намерения <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>. эта ошибка возникает в результате ошибки в клиенте резервного копирования в Windows Server 2003 и более поздних версиях. в Windows XP эта ошибка возвращается для преднамеренного завершения внешней последовательности резервного копирования.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:</strong> это возвращаемое значение введено в Windows Server 2003.</p><p>Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP:</strong> это возвращаемое значение вводится в Windows XP.</p><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p> | 
| <p>JET_errNoBackup</p> | <p>Не удалось выполнить операцию, так как не выполняется внешняя архивация.</p> | 
| <p>JET_errNotInitialized</p> | <p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>операция завершилась сбоем, так как была предпринята попытка использовать подсистему в устаревшем режиме (Windows 2000), где поддерживается только один экземпляр, когда в действительности несколько экземпляров уже существуют.</p> | 
| <p>JET_errTermInProgress</p> | <p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 



Если функция завершается успешно, Внешняя резервная копия была успешно выполнена. Успешное завершение означает, что все файлы (например, базы данных и журналы), подходящие для типа резервной копии (указанной в [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)), были получены из модуля резервного копирования. Резервные копии файлов можно восстановить с помощью жесткого восстановления ([жетекстерналресторе](./jetexternalrestore-function.md)).

В случае сбоя этой функции внешнее резервное копирование обычно завершается. Сбой означает, что резервная копия является недопустимой из-за ошибки использования клиента или приложения. Важно проверить код возврата для этого API, чтобы убедиться, что последовательность резервного копирования прошла успешно.

#### <a name="remarks"></a>Комментарии

Если для модуля настроено ведение журнала событий, в журнал заносится событие, указывающее на разрешение внешней резервной копии.

Если последовательность резервного копирования не завершена по порядку и при успешном вызове [жетендекстерналбаккуп](./jetendexternalbackup-function.md), последующие добавочные резервные копии могут содержать больше данных, чем ожидалось приложением.

Дополнительные сведения о последовательности API внешней резервной копии см. в разделе [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).

до Windows Vista, если усечение журнала не выполнялось, подсистема считалась резервной копией копии. Однако резервное копирование может быть обычной резервной копией, для которой не выполнялось усечение (например, при наличии отсоединенных баз данных). Параметр JET_bitBackupTruncateDone можно использовать для информирования ядра об этом и предоставления соответствующих изменений заголовка базы данных.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[Параметры обработки ошибок](./error-handling-parameters.md)  
[ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)  
[жетбегинекстерналбаккупинстанце](./jetbeginexternalbackupinstance-function.md)  
[жетклосефиле](./jetclosefile-function.md)  
[жетекстерналресторе](./jetexternalrestore-function.md)  
[жетжетаттачинфо](./jetgetattachinfo-function.md)  
[жетжетлогинфо](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетопенфиле](./jetopenfile-function.md)  
[жетреадфиле](./jetreadfile-function.md)  
[жетстопбаккуп](./jetstopbackup-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[жеттрункателог](./jettruncatelog-function.md)
