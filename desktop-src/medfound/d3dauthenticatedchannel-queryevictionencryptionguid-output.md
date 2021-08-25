---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY енкриптионвхенакцессиблегуид.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 01624b35b7c1b29267b490204a2d814adec1c7075eaf23e746e6ade04ceb0c6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942774"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a>\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуид

Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ Выходные данные запроса D3DAUTHENTICATEDCHANNEL**
</dt> <dd>

[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.

</dd> <dt>

**енкриптионгуидиндекс**
</dt> <dd>

Индекс GUID шифрования.

</dd> <dt>

**енкриптионгуид**
</dt> <dd>

Идентификатор GUID, указывающий поддерживаемый тип шифрования.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




