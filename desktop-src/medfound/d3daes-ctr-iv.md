---
description: Содержит вектор инициализации (IV) для шифрования блочного шифра в 128-битном режиме AES (AES-направление).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: Структура D3DAES_CTR_IV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 09535b432ff1af60ad33b622810d0d8a4d190cb81650214aa71b445ba3c22f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974793"
---
# <a name="d3daes_ctr_iv-structure"></a>Структура D3DAESного \_ \_ вектора

Содержит вектор инициализации (IV) для шифрования блочного шифра в 128-битном режиме AES (AES-направление).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a>Члены

<dl> <dt>

**IV**
</dt> <dd>

Вектор инициализации в формате с обратным порядком байтов.

</dd> <dt>

**Количество**
</dt> <dd>

Число блоков в формате с обратным порядком байтов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Структура **D3DAES \_ и \_ вектор** IV для [**DXVA2 \_ AES \_ \_**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) эквивалентны.

Дополнительные сведения см. в разделе [**DXVA2 AES с ключом \_ \_ \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (включение D3d9. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




