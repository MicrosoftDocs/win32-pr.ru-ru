---
description: Дополнительные сведения о функции Жетресеттаблесекуентиал
title: Функция Жетресеттаблесекуентиал
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 356fdcbf21dd3b08948936556b40f983ec1ac888
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985707"
---
# <a name="jetresettablesequential-function"></a>Функция Жетресеттаблесекуентиал


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetresettablesequential-function"></a>Функция Жетресеттаблесекуентиал

Функция **жетресеттаблесекуентиал** уведомляет ядро СУБД о том, что приложение больше не сканирует весь текущий индекс, содержащий данный курсор. Этот вызов обращается к отправке уведомления, отправленного [жетсеттаблесекуентиал](./jetsettablesequential-function.md).

**Windows xp:****жетресеттаблесекуентиал** появился в Windows XP.   

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*грбит*

Зарезервировано для последующего использования.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errTermInProgress</p> | <p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 



При успешном выполнении текущий индекс курсора больше не будет оптимизирован для последовательного просмотра всего индекса. Изменение состояния базы данных не выполняется.

В случае сбоя не произойдет никаких изменений в конфигурации курсора. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Комментарии

Этот вызов можно использовать для курсора, который ранее не был настроен с помощью вызова [жетсеттаблесекуентиал](./jetsettablesequential-function.md).

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетсеттаблесекуентиал](./jetsettablesequential-function.md)  
[жетстопсервице](./jetstopservice-function.md)
