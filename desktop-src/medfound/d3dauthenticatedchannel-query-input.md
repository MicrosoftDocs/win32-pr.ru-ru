---
description: 'Содержит входные данные для метода IDirect3DAuthenticatedChannel9:: Query.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: Структура D3DAUTHENTICATEDCHANNEL_QUERY_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262805"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a>\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL

Содержит входные данные для метода [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**QueryType**
</dt> <dd>

Идентификатор GUID, указывающий запрос. Список значений см. в разделе [запросы защита содержимого](content-protection-queries.md).

</dd> <dt>

**СПРАВИТЬСЯ**
</dt> <dd>

Маркер для аутентифицированного канала. Чтобы получить этот маркер, вызовите метод [**IDirect3DDevice9Video:: креатеаусентикатедчаннел**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**UINT**
</dt> <dd>

Порядковый номер запроса. В начале сеанса создайте криптографически защищенное 32-разрядное случайное число, которое будет использоваться в качестве начального порядкового номера. Для каждого запроса увеличьте порядковый номер на 1.

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

 

 




