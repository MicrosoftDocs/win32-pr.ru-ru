---
title: Структура WMDRM_ENCRYPT_SCATTER_BLOCK (Вмдрмсдк. h)
description: '\_ \_ \_ Структура блочной точечной файловой структуры содержит блок данных для шифрования.'
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- Формат WMDRM_ENCRYPT_SCATTER_BLOCK структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258cb7e0d8d2cac8da40197aaa45028a56af0ff3a313d65c1a98c50d45b8d3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658164"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>\_ \_ \_ Структура блочного блока WMDRM Encrypt

Структура **\_ \_ \_ блочной точечной файловой** структуры содержит блок данных для шифрования.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двстреамид**
</dt> <dd>

Идентификатор потока, которому принадлежит блок данных.

</dd> <dt>

**кбблокк**
</dt> <dd>

Размер блока в байтах.

</dd> <dt>

**пбблокк**
</dt> <dd>

Указатель на буфер, содержащий блок данных.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура используется методом [**ивмдрменкриптскаттер:: енкриптскаттер**](iwmdrmencryptscatter-encryptscatter.md) для обнаружения блоков данных для шифрования.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





