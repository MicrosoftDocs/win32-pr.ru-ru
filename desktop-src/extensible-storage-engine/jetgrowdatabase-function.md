---
description: Дополнительные сведения о функции Жетгровдатабасе
title: Функция Жетгровдатабасе
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 710e41b29c55ec435db6eb1b9e1536740819478e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479070"
---
# <a name="jetgrowdatabase-function"></a>Функция Жетгровдатабасе


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgrowdatabase-function"></a>Функция Жетгровдатабасе

Функция **жетгровдатабасе** расширяет размер открытой в данный момент базы данных.

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*DBID*

База данных, которая будет расширена.

*CPG*

Требуемый размер базы данных на страницах.

*пкпгреал*

Указатель на число, которое получает размер базы данных на страницах после вызова API. Если вызов API завершается неудачей, содержимое *пкпгреал* не определяется.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errDiskFull</p> | <p>Недостаточно свободного места на томе для выполнения операции увеличения.</p> | 
| <p>JET_errDiskIO</p> | <p><a href="gg269242(v=exchg.10).md">Жетсетдатабасесизе</a>вернул ошибку, связанную с файлом. Дополнительные сведения о других ошибках, связанных с файлами, которые могут быть возвращены, см. в разделе <a href="gg269242(v=exchg.10).md">жетсетдатабасесизе</a>.</p> | 



#### <a name="remarks"></a>Комментарии

Если **жетгровдатабасе** вызывается до вставки больших объемов данных, то файл базы данных будет увеличен за одну операцию. Это снизит вероятность того, что файл базы данных станет фрагментированным на уровне файловой системы, а также сократит число попыток увеличения размера файла базы данных. Увеличение файла базы данных выполняется один раз быстрее, чем в несколько раз.

В настоящее время поддерживается только увеличение размера файла. Чтобы сжать файл, используйте функцию дефрагментации служебной программы **esentutl.exe** .

Сведения о том, как задать размер открытой базы данных, см. в разделе [жетсетдатабасесизе](./jetsetdatabasesize-function.md).

Размер файла может не совпадать с количеством страниц, возвращаемых в *пкпгреал*. Существует два дополнительных зарезервированных страницы, которые могут не учитываться в *пкпгреал*.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[жетсетдатабасесизе](./jetsetdatabasesize-function.md)
