---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY аутпутид.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9861de1dc97a606821060fcb7665cac557a08c084271c319c3804740169af7d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600784"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a>\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куерираутпутид

Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ аутпутид**](d3dauthenticatedquery-outputid.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ Выходные данные запроса D3DAUTHENTICATEDCHANNEL**
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

**аутпутидиндекс**
</dt> <dd>

Индекс выходного идентификатора, заданного в элементе **аутпутид** .

</dd> <dt>

**аутпутид**
</dt> <dd>

Идентификатор выхода, связанный с указанным устройством и сеансом шифрования.

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

 

 




