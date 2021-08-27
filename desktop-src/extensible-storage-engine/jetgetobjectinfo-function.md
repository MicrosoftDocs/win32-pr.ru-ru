---
description: Дополнительные сведения о функции Жетжетобжектинфо
title: Функция JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e6317280c5e794e9809c15f47f01d55ffd48eeb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982427"
---
# <a name="jetgetobjectinfo-function"></a>Функция JetGetObjectInfo


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgetobjectinfo-function"></a>Функция JetGetObjectInfo

Функция **жетжетобжектинфо** извлекает сведения об объектах базы данных. В настоящее время поддерживаются только таблицы. [Жетжеттаблеинфо](./jetgettableinfo-function.md) можно использовать для получения дополнительных сведений, чем **жетжетобжектинфо**.

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Используемый контекст сеанса базы данных.

*DBID*

База данных, из которой извлекаются данные.

*обжтип*

Объекты, содержащие сведения для извлечения. В настоящее время поддерживаются только JET_objtypNil и JET_objtypTable, которые ведут себя одинаково. Будут получены только таблицы.

*сзконтаинернаме*

Этот параметр зарезервирован для будущего использования и передает **значение NULL**. Имена типов объектов, сведения о которых необходимо получить.

*сзобжектнаме*

Имя объекта, который содержит извлекаемые данные. Если *инфолевел* использует параметры JET_ObjInfoList или JET_ObjInfoListNoStats для получения списка всех объектов, это значение должно быть **равно NULL** или быть пустой строкой.

В настоящее время поддерживаются только имена таблиц.

*пвресулт*

Указатель на буфер, который получает указанные сведения.

Размер буфера в байтах передается в *кбмакс*. При сбое содержимое *пвресулт* не определено.

Сведения, хранящиеся в *пвресулт* , зависят от *инфолевел*.

*кбмакс*

Размер буфера (в байтах), переданного в *пвресулт*.

*инфолевел*

Указывает, какой тип данных получить для указанного объекта. Это влияет на интерпретацию *пвресулт* .

Для этого параметра можно задать следующие параметры.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_ObjInfo</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</p><p>Структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> заполняется сведениями, относящимися к объекту с именем в <em>сзобжектнаме</em>.</p><p>Если вызывающему объекту не требуется знание количества записей и страниц для объекта, рекомендуется использовать JET_ObjInfoNoStats уровень информации, который может быть быстрее, так как статистика не включена.</p> | 
| <p>JET_ObjInfoList</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Извлекаются сведения обо всех объектах. Будет создана временная таблица, а сведения, необходимые для обхода временной таблицы, описаны в структуре <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Дополнительные сведения см. в разделе <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. Если вызывающему объекту не требуется знание количества записей и страниц для объекта, рассмотрите возможность использования JET_ObjInfoListNoStats, что может быть быстрее.</p> | 
| <p>JET_ObjInfoListACM</p> | <p>Не рекомендуется и не поддерживается в настоящее время.</p> | 
| <p>JET_ObjInfoListNoStats</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Извлекаются сведения обо всех объектах. Будет создана временная таблица, а сведения, необходимые для обхода временной таблицы, описаны в структуре <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Дополнительные сведения см. в разделе <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. JET_ObjInfoListNoStats идентично JET_ObjInfoList, за исключением того, что столбцы, сообщающие о количестве записей (<em>колумнидкрекорд</em>) и страницах (<em>колумнидкпаже</em>), не обновляются.</p> | 
| <p>JET_ObjInfoMax</p> | <p><em>пвресулт</em> интерпретируется как <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Максимальный размер объекта находится на страницах. В настоящее время возвращаются только таблицы.</p> | 
| <p>JET_ObjInfoNoStats</p> | <p><em>пвресулт</em> интерпретируется как <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Будут получены сведения только о объекте, указанном в <em>сзобжектнаме</em> .</p><p>Структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> будет заполнена сведениями, относящимися к объекту с именем в <em>сзобжектнаме</em>.</p><p>JET_ObjInfoNoStats идентично JET_ObjInfo, за исключением того, что поля, сообщающие число записей и страниц, имеют нулевое значение.</p> | 
| <p>JET_ObjInfoRulesLoaded</p> | <p>Не рекомендуется и не поддерживается в настоящее время.</p> | 
| <p>JET_ObjInfoSysTabCursor</p> | <p>Не рекомендуется и не поддерживается в настоящее время.</p> | 
| <p>JET_ObjInfoSysTabReadOnly</p> | <p>Не рекомендуется и не поддерживается в настоящее время.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Размер буфера, заданного в <em>кбмакс</em> , слишком мал для хранения требуемой информации.</p> | 
| <p>JET_errInvalidName</p> | <p>В <em>сзобжектнаме</em> или <em>сзконтаинернаме</em>было указано недопустимое имя.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Передан неверный параметр. Возможно, в <em>инфолевел</em>был передан недопустимый уровень.</p> | 



#### <a name="remarks"></a>Комментарии

Если **жетжетобжектинфо** успешно создает временную таблицу (например, JET_ObjInfoList или JET_ObjInfoNoStats), вызывающий объект отвечает за закрытие временной таблицы с помощью [жетклосетабле](./jetclosetable-function.md).

В настоящее время **жетжетобжектинфо** поддерживает только получение сведений о таблицах.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетжетобжектинфов</strong> (Юникод) и <strong>жетжетобжектинфоа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетжеттаблеинфо](./jetgettableinfo-function.md)
