---
description: Указывает разрешения на управление доступом для каталога на смарт-карте.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Перечисление CARD_DIRECTORY_ACCESS_CONDITION (Cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263007"
---
# <a name="card_directory_access_condition-enumeration"></a>\_ \_ Перечисление условий доступа к КАТАЛОГу карты \_

Перечисление **\_ \_ \_ условий доступа к каталогу карты** определяет разрешения на управление доступом для каталога на [*смарт-карте*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**инвалидак**
</dt> <dd>

Недопустимое значение.

</dd> <dt>

<span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**усеркреатеделетедирак**
</dt> <dd>

Конкретные пользователи могут читать, записывать и удалять каталог.

</dd> <dt>

<span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**админкреатеделетедирак**
</dt> <dd>

Администраторы могут читать, записывать и удалять каталог.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, \[ только классические приложения Windows XP\]<br/>                              |
| Минимальная версия сервера<br/> | Windows Server 2003, \[ только для настольных приложений Windows server 2003\]<br/>            |
| Header<br/>                   | <dl> <dt>Cardmod. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поставщик службы криптографии для смарт-карт (Майкрософт)](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**кардкреатедиректори**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**кардделетедиректори**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
