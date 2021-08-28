---
description: 'Дополнительные сведения: функция обратного вызова JET_CALLBACK'
title: Функция обратного вызова JET_CALLBACK
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08d992d1e8b6ca7c6a987a57f44b48d6ba291328
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471176"
---
# <a name="jet_callback-callback-function"></a>Функция обратного вызова JET_CALLBACK


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_callback-callback-function"></a>Функция обратного вызова JET_CALLBACK

Функция **JET_CALLBACK** — это функция обратного вызова с несколькими целями, используемая ядром СУБД для информирования приложения о событии, включающем в себя уведомления о дефрагментации и состоянии курсора в оперативном режиме.

В разделе [JET_CBTYP](./jet-cbtyp.md) конкретные параметры, используемые для параметров этой функции, так как эти параметры будут различаться в зависимости от параметра **JET_CBTYP** , выбранного для использования в параметре *кбтип* .

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, для которого выполняется обратный вызов.

*DBID*

База данных, для которой выполняется обратный вызов.

*TableID*

Курсор, для которого выполняется обратный вызов.

*кбтип*

Точка в операции, в которой производится обратный вызов. Список значений и значения следующих параметров в каждом случае см. в разделе [JET_CBTYP](./jet-cbtyp.md) .

*pvArg1*

Параметр, используемый для взаимодействия с приложением с помощью обратного вызова. Сведения об использовании этого параметра для каждого обратного вызова, поддерживаемого ядром СУБД, см. в разделе [JET_CBTYP](./jet-cbtyp.md) .

*pvArg2*

Параметр, используемый для взаимодействия с приложением с помощью обратного вызова. Сведения об использовании этого параметра для каждого обратного вызова, поддерживаемого ядром СУБД, см. в разделе [JET_CBTYP](./jet-cbtyp.md) .

*пвконтекст*

Параметр, используемый для взаимодействия с приложением с помощью обратного вызова. Сведения об использовании этого параметра для каждого обратного вызова, поддерживаемого ядром СУБД, см. в разделе [JET_CBTYP](./jet-cbtyp.md) .

*улунусед*

Параметр, используемый для взаимодействия с приложением с помощью обратного вызова. Сведения об использовании этого параметра для каждого обратного вызова, поддерживаемого ядром СУБД, см. в разделе [JET_CBTYP](./jet-cbtyp.md) .

#### <a name="return-value"></a>Возвращаемое значение

функция возвращает один из [расширенных кодов ошибок ядра служба хранилища](./extensible-storage-engine-error-codes.md). сведения о том, как вернуть эти коды в виде значений hresult, см. в разделе [ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md). При успешном выполнении операция, выдала ответный вызов, может продолжать работу в обычном режиме. В некоторых случаях обратный вызов может возвращать предупреждение, которое влияет на эту операцию. Сведения об использовании этих предупреждений в операции см. в разделе [JET_CBTYP](./jet-cbtyp.md) .

В случае сбоя операция, выдала ответный вызов, может продолжаться обычным образом или не работать. Сведения об использовании кода ошибки в операции см. в разделе [JET_CBTYP](./jet-cbtyp.md) .

#### <a name="remarks"></a>Комментарии

Если обратный вызов передает приложению курсор, то важно помнить, что этот курсор намеренно ограничен небольшим набором функций, чтобы избежать рекурсии и других углинесс. Допустимы следующие операции:

  - [жетдупкурсор](./jetdupcursor-function.md)

  - [жетенумератеколумнс](./jetenumeratecolumns-function.md)

  - [жетжетбукмарк](./jetgetbookmark-function.md)

  - [жетжеткуррентиндекс](./jetgetcurrentindex-function.md)

  - [жетжеткурсоринфо](./jetgetcursorinfo-function.md)

  - [жетжетлс](./jetgetls-function.md)

  - [жетжетрекордпоситион](./jetgetrecordposition-function.md)

  - [жетжетсекондариндексбукмарк](./jetgetsecondaryindexbookmark-function.md)

  - [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md)

  - [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)

  - [жетжеттаблеинфо](./jetgettableinfo-function.md)

  - [жетрегистеркаллбакк](./jetregistercallback-function.md)

  - [жетретриевеколумн](./jetretrievecolumn-function.md)

  - [жетретриевеколумнс](./jetretrievecolumns-function.md)

  - [жетретриевекэй](./jetretrievekey-function.md)

  - [жетсетколумн](./jetsetcolumn-function.md)

  - [жетсетколумнс](./jetsetcolumns-function.md)

  - [жетсетлс](./jetsetls-function.md)

  - [жетунрегистеркаллбакк](./jetunregistercallback-function.md)

При проектировании обратного вызова примите во внимание, что даже с этими ограничениями по-прежнему может произойти сбой обратного вызова.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
