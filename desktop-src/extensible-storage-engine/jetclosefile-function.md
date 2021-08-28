---
description: Дополнительные сведения о функции Жетклосефиле
title: Функция Жетклосефиле
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad8f40f53ec23a5a555efeb270370d384d6dc9a6
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989057"
---
# <a name="jetclosefile-function"></a>Функция Жетклосефиле


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetclosefile-function"></a>Функция Жетклосефиле

Функция **жетклосефиле** закрывает файл, Открытый в [жетопенфиле](./jetopenfile-function.md) , после извлечения данных из этого файла с помощью [жетреадфиле](./jetreadfile-function.md).

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Параметры

*хффиле*

Описатель файла для чтения.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p><p>эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти для <strong>жетклосефиле</strong> в следующих случаях:</p><ul><li><p>указан недопустимый дескриптор экземпляра (Windows XP и более поздних версий),</p></li><li><p>Указанный описатель файла недопустим.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>Не удалось выполнить операцию, так как не выполняется внешняя архивация.</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (Windows 2000), где поддерживается только один экземпляр, если в действительности несколько экземпляров уже существуют.</p> | 
| <p>JET_errTermInProgress</p> | <p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 



При успешном выполнении маркер файла закрывается. Если файл базы данных был закрыт, то связанный с ним файл исправления базы данных (если таковой имеется) уничтожается.

При сбое изменения не происходят.

#### <a name="remarks"></a>Комментарии

В настоящее время ядро СУБД поддерживает только один открытый файл через [жетопенфиле](./jetopenfile-function.md) . Если маркер файла открыт с помощью [жетопенфиле](./jetopenfile-function.md) , его необходимо закрыть с помощью **жетклосефиле** , прежде чем можно будет открыть другой файл.

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
[JET_INSTANCE](./jet-instance.md)  
[JET_HANDLE](./jet-handle.md)  
[жетопенфиле](./jetopenfile-function.md)  
[жетреадфиле](./jetreadfile-function.md)  
[жетстопсервице](./jetstopservice-function.md)
