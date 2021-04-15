---
description: Указывает разрешения на управление доступом для файла на смарт-карте.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Перечисление CARD_FILE_ACCESS_CONDITION (Cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662365"
---
# <a name="card_file_access_condition-enumeration"></a>\_ \_ Перечисление условий доступа к файлу карты \_

Перечисление **\_ \_ \_ условий доступа к файлу карты** определяет разрешения на управление доступом для файла на [*смарт-карте*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**инвалидак**
</dt> <dd>

Недопустимое значение.

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**еверйонереадусервритеак**
</dt> <dd>

Все могут читать файл. Определенные пользователи могут записывать в файл.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**усервритиксекутеак**
</dt> <dd>

Только определенные пользователи могут выполнять чтение и запись в файл.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**еверйонереададминвритеак**
</dt> <dd>

Все могут читать файл. Администраторы могут записывать в файл.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**ункновнак**
</dt> <dd>

Разрешения на доступ к файлу неизвестны.

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

[**\_ \_ сведения о файле карты**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**кардкреатефиле**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
