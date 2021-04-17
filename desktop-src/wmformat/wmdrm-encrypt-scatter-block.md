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
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721015"
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

## <a name="remarks"></a>Комментарии

Эта структура используется методом [**ивмдрменкриптскаттер:: енкриптскаттер**](iwmdrmencryptscatter-encryptscatter.md) для обнаружения блоков данных для шифрования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





