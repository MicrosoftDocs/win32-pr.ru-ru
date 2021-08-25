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
ms.openlocfilehash: 8038179c7337edaff0138fc46c34191f99821250808c4ace16dc76cdfafd3b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878964"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows xp, только для \[ настольных приложений Windows xp\]<br/>                              |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows server 2003 \[ только классические приложения\]<br/>            |
| Заголовок<br/>                   | <dl> <dt>Cardmod. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Поставщик службы криптографии для смарт-карт (Майкрософт)](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**кардкреатедиректори**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**кардделетедиректори**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
