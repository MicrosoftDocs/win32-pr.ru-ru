---
description: Содержит входные данные для \_ запроса D3DAUTHENTICATEDQUERY аутпутидкаунт.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2fc43d10b497b4ab904cbec551a41d240fca33bd395ae2f4093d5b9d25067816
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449474"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a>\_ \_ Входная структура D3DAUTHENTICATEDCHANNEL куерйоутпутидкаунт

Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**](d3dauthenticatedquery-outputidcount.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Ввод**
</dt> <dd>

[**\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) , содержащая идентификатор GUID для запроса и других данных.

</dd> <dt>

**девицехандле**
</dt> <dd>

Маркер устройства.

</dd> <dt>

**криптосессионхандле**
</dt> <dd>

Маркер сеанса шифрования.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




