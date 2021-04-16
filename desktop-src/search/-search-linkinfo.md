---
description: Хранит сведения о типах ссылок и используется интерфейсом Иитемпревиеверекст.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Структура ЛИНКИНФО
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262940"
---
# <a name="linkinfo-structure"></a>Структура ЛИНКИНФО

\[**Линкинфо** и [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживаются только в Windows XP и Windows Server 2003 и больше не должны использоваться.\]

Хранит сведения о типах ссылок и используется интерфейсом [**иитемпревиеверекст**](-search-iitempreviewerext.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**type**
</dt> <dd>

Тип: **/с [](-search-linktype.md)**

</dd> <dd>

Тип ссылки, указанный при обходе или индексировании [**, указанном константой**](-search-linktype.md) типа "ссылка".

</dd> <dt>

**бстрконтенттипе**
</dt> <dd>

Тип: **BSTR**

</dd> <dd>

Значение **BSTR** , указывающее тип содержимого.

</dd> <dt>

**бстренкодинг**
</dt> <dd>

Тип: **BSTR**

</dd> <dd>

Атрибут EncodingStyle, указанный в файле языка описания веб-служб (WSDL).

</dd> <dt>

**бстрфиликст**
</dt> <dd>

Тип: **BSTR**

</dd> <dd>

Значение **BSTR** , указывающее расширение имени файла.

</dd> <dt>

**вардата**
</dt> <dd>

Тип: **Variant**

</dd> <dd>

Вариант, указывающий значение переменной.

</dd> <dt>

**дврелатедпартс**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Значение **типа DWORD** , указывающее связанные части.

</dd> <dt>

**бстррелатедЦид**
</dt> <dd>

Тип: **BSTR**

</dd> <dd>

Значение **BSTR** , указывающее свойство CID, десятичную строку со знаком, которая является незаполненной.

</dd> <dt>

**лкодепаже**
</dt> <dd>

Тип: **Long**

</dd> <dd>

Кодовая страница, используемая для кодирования строки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для предварительного просмотра вложений с помощью обработчика протокола стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать структуру **линкинфо** и следующие API: методы [**Иитемпревиеверекст:: жетлинкедконтент**](-search-iitempreviewerext-getlinkedcontent.md) и [**иитемпревиеверекст:: жетрелатедпарт**](-search-iitempreviewerext-getrelatedpart.md) и [**перечисление**](-search-linktype.md) типов ссылок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Распространяемые компоненты<br/>          | Поиск на рабочем столе Windows (WDS) 3,0<br/>          |



 

 




