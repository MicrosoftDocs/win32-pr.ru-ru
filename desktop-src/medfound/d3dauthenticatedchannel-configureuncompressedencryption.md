---
description: Содержит входные данные для \_ команды D3DAUTHENTICATEDCONFIGURE енкриптионвхенакцессибле.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 661f4cd043a2337aa499aaa165c16d2e1fdf41f8e87826412250ea0fe85c47a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062004"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a>\_Структура КОНФИГУРЕУНКОМПРЕССЕДЕНКРИПТИОН D3DAUTHENTICATEDCHANNEL

Содержит входные данные для команды [**D3DAUTHENTICATEDCONFIGURE \_ енкриптионвхенакцессибле**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a>Члены

<dl> <dt>

**Параметры**
</dt> <dd>

[**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной**](d3dauthenticatedchannel-configure-input.md) структуры, которая содержит идентификатор GUID команды и другие данные.

</dd> <dt>

**енкриптионгуид**
</dt> <dd>

Идентификатор GUID, указывающий тип применяемого шифрования.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




