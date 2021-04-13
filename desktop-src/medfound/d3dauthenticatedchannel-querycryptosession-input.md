---
description: Содержит входные данные для \_ запроса D3DAUTHENTICATEDQUERY CRYPTOSESSION.
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 76b9d09bcb03dbf3742d551c253d3f4982215757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342525"
---
# <a name="d3dauthenticatedchannel_querycryptosession_input-structure"></a>\_ \_ Входная структура D3DAUTHENTICATEDCHANNEL куерикриптосессион

Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DXVA2DecodeHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Ввод**
</dt> <dd>

[**\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) , содержащая идентификатор GUID для запроса и других данных.

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

Маркер устройства декодера DirectX Video Acceleration 2 (ДКСВА-2).

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

 

 




