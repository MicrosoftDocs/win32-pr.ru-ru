---
description: Дополнительные сведения о функции Жетсетдатабасесизе
title: Функция Жетсетдатабасесизе
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27799dbdbc21af4421713828633199d1c1a18973
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466232"
---
# <a name="jetsetdatabasesize-function"></a>Функция Жетсетдатабасесизе


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetsetdatabasesize-function"></a>Функция Жетсетдатабасесизе

Функция **жетсетдатабасесизе** задает размер неоткрытого файла базы данных.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Определяет контекст сеанса базы данных, используемый для вызова API.

*сздатабасенаме*

Определяет имя файла базы данных, размер которого необходимо изменить.

*CPG*

Задает требуемый размер базы данных на страницах.

*пкпгреал*

Указатель на число, которое получает размер базы данных на страницах после вызова API. Если вызов API завершился неудачно, содержимое *пкпгреал* не определено.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errDatabaseInconsistent<br />JET_errDatabaseDirtyShutdown</p> | <p>JET_errDatabaseInconsistent и JET_errDatabaseDirtyShutdown имеют одно и то же числовое значение. База данных, размер которой необходимо настроить, должен быть в состоянии чистого отключения, известного как противоречивое состояние. Непоследовательная база данных не повреждена, но она требует воспроизведения файлов журнала.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>сздатабасенаме</em> не может быть пустой строкой, отличной от NULL.</p> | 
| <p>JET_errDiskFull</p> | <p>Недостаточно свободного места на томе для выполнения операции увеличения. <strong>Жетсетдатабасесизе</strong> также может возвращать множество ошибок, связанных с файлами, включая, но не ограничиваясь:</p><ul><li><p>JET_errDiskIO</p></li><li><p>JET_errFileNotFound</p></li><li><p>JET_errInvalidPath</p></li><li><p>JET_errFileAccessDenied</p></li><li><p>JET_errOutOfFileHandles</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Одна из причин, по которой эта ошибка может быть возвращена, — если <em>CPG</em> соответствует минимальному размеру базы данных. Текущий минимальный размер базы данных — 256 страниц.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Системе не хватает ресурсов памяти.</p> | 



#### <a name="remarks"></a>Комментарии

Если **жетсетдатабасесизе** вызывается до вставки больших объемов данных, то файл базы данных будет увеличен за одну операцию. Это снизит вероятность того, что файл базы данных станет фрагментированным на уровне файловой системы, а также сократит число попыток увеличения размера файла базы данных. Увеличение файла базы данных выполняется один раз быстрее, чем в несколько раз.

В настоящее время поддерживается только увеличение размера файла. Чтобы сжать файл, используйте функцию дефрагментации служебной программы esentutl.exe.

Если *CPG* меньше текущего размера базы данных, операция будет пропущена. Если *CPG* меньше, чем минимальный размер базы данных (в настоящее время 256 страниц), он возвратит JET_errInvalidParameter.

Чтобы задать размер открытой базы данных, см. раздел [жетгровдатабасе](./jetgrowdatabase-function.md).

Размер файла может не совпадать с количеством страниц, возвращаемых в *пкпгреал*. Существует два дополнительных зарезервированных страницы, которые не могут быть учтены в *пкпгреал*.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетсетдатабасесизев</strong> (Юникод) и <strong>жетсетдатабасесизеа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[жетгровдатабасе](./jetgrowdatabase-function.md)
