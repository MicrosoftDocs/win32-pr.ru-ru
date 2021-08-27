---
description: Дополнительные сведения о функции Жетстопбаккупинстанце
title: Функция Жетстопбаккупинстанце
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4dae676cfbbb0f2509a7d86fbb6507b8e2110f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987247"
---
# <a name="jetstopbackupinstance-function"></a>Функция Жетстопбаккупинстанце


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetstopbackupinstance-function"></a>Функция Жетстопбаккупинстанце

Функция **жетстопбаккупинстанце** предотвращает продолжение потоковой операции резервного копирования на определенном работающем экземпляре, тем самым завершая потоковую архивацию предсказуемым образом.

**Windows xp:****жетстопбаккупинстанце** появился в Windows XP.  

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Определяет выполняющийся экземпляр, используемый для вызова API.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Указанный параметр экземпляра имеет недопустимое значение (а не экземпляр, который сейчас выполняется).</p><p><strong>Windows XP:</strong>  это возвращаемое значение вводится в Windows XP.</p> | 



Если эта функция завершается успешно, указанный экземпляр будет запускать любые новые API-интерфейсы потоковой архивации.

Если эта функция завершается ошибкой, то не будет выполнено никаких действий для подготовки к завершению резервного копирования на экземпляре, и изменение состояния экземпляра не будет выполнено.

#### <a name="remarks"></a>Комментарии

Резервное копирование обычно запускается событием за пределами механизма обработки и с помощью этого API, а само приложение ESENT делает все последующие вызовы интерфейсов API потоковой архивации неудачными. Большинство API-интерфейсов потоковой архивации начнут завершаться сбоем с JET_errBackupAbortByServer. Таким образом, любое выполнение потоковой архивации (например, [жетреадфилеинстанце](./jetreadfileinstance-function.md)) вернет ошибку. Операции резервного копирования, которые являются частью завершения резервного копирования (например, [жетендекстерналбаккупинстанце](./jetendexternalbackupinstance-function.md)), будут по-прежнему разрешены.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетендекстерналбаккупинстанце](./jetendexternalbackupinstance-function.md)  
[жетреадфилеинстанце](./jetreadfileinstance-function.md)  
[жетстопсервице](./jetstopservice-function.md)
