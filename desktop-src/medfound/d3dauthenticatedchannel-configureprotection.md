---
description: Содержит входные данные для \_ команды защиты D3DAUTHENTICATEDCONFIGURE.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fc1daee7bfd9320539a03974ab431c4ba588d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896577"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a>\_Структура КОНФИГУРЕПРОТЕКТИОН D3DAUTHENTICATEDCHANNEL

Содержит входные данные для [**команды \_ защиты D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a>Члены

<dl> <dt>

**Параметры**
</dt> <dd>

[**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной**](d3dauthenticatedchannel-configure-input.md) структуры, которая содержит идентификатор GUID команды и другие данные.

</dd> <dt>

**Защиты**
</dt> <dd>

Структура [**\_ \_ флагов защиты D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) , указывающая уровень защиты.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                             |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




