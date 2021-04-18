---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY енкриптионвхенакцессиблегуидкаунт.
ms.assetid: 168f9455-8dc6-473a-ad2c-e51996b63650
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 51668dccdfa15649ec2a062a1231eb0b16e68ff8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701321"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguidcount_output-structure"></a>\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуидкаунт

Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуидкаунт**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  NumEncryptionGuids                   UINT;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Выходные данные**
</dt> <dd>

[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.

</dd> <dt>

**UINT**
</dt> <dd>

Число идентификаторов GUID шифрования.

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

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




