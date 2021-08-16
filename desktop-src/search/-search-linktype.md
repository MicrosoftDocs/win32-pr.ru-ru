---
description: Указывает тип ссылки при обходе или индексировании.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Перечисление типов ссылок
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 16c61f8d92a6f90be0fa4b64ddd9d582987ac0bdf52ca1c596c7db3a7fa4b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463047"
---
# <a name="linktype-enumeration"></a>Перечисление типов ссылок

\[перечисление типов ссылок поддерживается **только в Windows** XP и Windows Server 2003 и больше не должно использоваться.\]

Указывает тип ссылки при обходе или индексировании.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**\_URL-адрес ссылок**
</dt> <dd>

Указывает, следует ли индексировать тип ссылки URL-адресов.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**\_содержимое ссылок**
</dt> <dd>

Указывает, следует ли индексировать содержимое ссылки.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**\_с/с**
</dt> <dd>

Указывает связанную ссылку.

</dd> </dl>

## <a name="remarks"></a>Remarks

для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться **использовать флаги** [**иитемпревиеверекст:: жетлинкедконтент**](-search-iitempreviewerext-getlinkedcontent.md) и [**иитемпревиеверекст:: жетрелатедпарт**](-search-iitempreviewerext-getrelatedpart.md) и структуру [**линкинфо**](-search-linkinfo.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



 

 




