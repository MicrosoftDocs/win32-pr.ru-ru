---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY аутпутидкаунт.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: c97f55d05aff3feb1857456ec04c4fa48872487decc5812912081b894896dce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777554"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a>\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куерйоутпутидкаунт

Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**](d3dauthenticatedquery-outputidcount.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Выходные данные**
</dt> <dd>

[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.

</dd> <dt>

**девицехандле**
</dt> <dd>

Маркер устройства.

</dd> <dt>

**криптосессионхандле**
</dt> <dd>

Маркер сеанса шифрования.

</dd> <dt>

**нумаутпутидс**
</dt> <dd>

Число идентификаторов выходных данных, связанных с указанным устройством и сеансом шифрования.

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

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




