---
description: Дополнительные сведения о функции Жетжетиндексинфо
title: Функция JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4d7c835d5077d2bfee87025b202480a888de981
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988587"
---
# <a name="jetgetindexinfo-function"></a>Функция JetGetIndexInfo


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgetindexinfo-function"></a>Функция JetGetIndexInfo

Функция **жетжетиндексинфо** получает сведения о индексе.

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*DBID*

Идентификатор базы данных, используемый для вызова API.

*сзтабленаме*

Имя таблицы, содержащей индекс, с извлекаемыми данными.

*сзиндекснаме*

Имя индекса с извлекаемыми данными.

*пвресулт*

Указатель на буфер, который будет принимать нужные сведения. Буфер должен быть согласован, чтобы вместить требуемый тип. Тип буфера зависит от параметра *инфолевел* .

*кбресулт*

Размер (в байтах) буфера, переданного в качестве *пвресулт*.

*инфолевел*

Сведения, которые будут храниться в *пвресулт*. Для этого параметра можно использовать следующие параметры.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_IdxInfo</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . При успешном выполнении структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> получает сведения об индексе. При сбое содержимое <em>пвбуффер</em> не определено.</p> | 
| <p>JET_IdxInfoCount</p> | <p><em>пвресулт</em> интерпретируется как ULong. В случае успеха ULONG содержит количество индексов в указанной таблице. <em>сзиндекснаме</em> игнорируется. При сбое содержимое <em>пвбуффер</em> не определено.</p> | 
| <p>JET_IdxInfoIndexId</p> | <p><em>пвресулт</em> интерпретируется как <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. При успешном выполнении структура <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> получает сведения об индексе. При сбое содержимое <em>пвбуффер</em> не определено.</p> | 
| <p>JET_IdxInfoLangid</p> | <p>JET_IdxInfoLangid не рекомендуется к использованию. Вместо этого используйте JET_IdxInfoLCID и макрос <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">лангидфромлЦид</a> .</p> | 
| <p>JET_IdxInfoLCID</p> | <p><em>пвресулт</em> интерпретируется как LCID. При успешном выполнении код LCID содержит идентификатор локали индекса. При сбое содержимое <em>пвбуффер</em> не определено.</p><p><strong>Windows XP:</strong> JET_IdxInfoLCID введены в Windows XP.</p> | 
| <p>JET_IdxInfoList</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . При успешном выполнении структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> получает сведения об индексе. При сбое содержимое <em>пвбуффер</em> не определено.</p> | 
| <p>JET_IdxInfoOLC</p> | <p>JET_IdxInfoOLC устарел.</p> | 
| <p>JET_IdxInfoResetOLC</p> | <p>JET_IdxInfoResetOLC устарел.</p> | 
| <p>JET_IdxInfoSpaceAlloc</p> | <p><em>пвресулт</em> интерпретируется как ULong. При успешном выполнении в ULONG содержится место использования индекса. При сбое содержимое <em>пвбуффер</em> не определено.</p> | 
| <p>JET_IdxInfoSysTabCursor</p> | <p>JET_IdxInfoSysTabCursor устарел.</p> | 
| <p>JET_IdxInfoVarSegMac</p> | <p><em>пвресулт</em> интерпретируется как ushort. При успешном выполнении объект USHORT содержит значение <em>кбварсегмак</em> , используемое при создании индекса. Описание <em>кбварсегмак</em>см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . При сбое содержимое <em>пвбуффер</em> не определено.</p> | 
| <p>JET_IdxInfoKeyMost</p> | <p><em>пвресулт</em> интерпретируется как ushort. При успешном выполнении объект USHORT содержит значение <em>кбкэймост</em> , используемое при создании индекса. Описание <em>кбкэймост</em>см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . При сбое содержимое <em>пвбуффер</em> не определено.</p><p><strong>Windows Vista:</strong> JET_IdxInfoKeyMost введены в Windows Vista.</p> | 
| <p>JET_IdxInfoCreateIndex</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . При сбое содержимое <em>пвбуффер</em> не определено.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex представлен в Windows 7.</p> | 
| <p>JET_IdxInfoCreateIndex2</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . При сбое содержимое <em>пвбуффер</em> не определено.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex2 представлен в Windows 7.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errIndexNotFound</p> | <p>Указанный индекс не найден в указанной таблице.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Буфер, переданный как <em>пвресулт</em> , слишком мал. Содержимое буфера не определено.</p> | 



#### <a name="remarks"></a>Комментарии

**Жетжетиндексинфо** и [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md) извлекают идентичные сведения о индексе. Разница заключается в том, как указана таблица. **Жетжетиндексинфо** ждет базу данных (*DBID*) и имя таблицы (*сзтабленаме*), а [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md) — идентификатор таблицы (*TableID*).

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетжетиндексинфов</strong> (Юникод) и <strong>жетжетиндексинфоа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)
