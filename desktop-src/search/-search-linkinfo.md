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
ms.openlocfilehash: 97c106a5a819ac1068501c77555f3eae238c935e2262894c6c250dfc6782188f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863947"
---
# <a name="linkinfo-structure"></a>Структура ЛИНКИНФО

\[**линкинфо** и [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживаются только в Windows XP и Windows Server 2003 и больше не должны использоваться.\]

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

## <a name="remarks"></a>Remarks

для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать структуру **линкинфо** и следующие api: методы [**иитемпревиеверекст:: жетлинкедконтент**](-search-iitempreviewerext-getlinkedcontent.md) и [**иитемпревиеверекст:: жетрелатедпарт**](-search-iitempreviewerext-getrelatedpart.md) и [**перечисление**](-search-linktype.md) типов ссылок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 3,0<br/>          |



 

 




