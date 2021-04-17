---
title: Структура WMDRM_ENCRYPT_SCATTER_INFO (Вмдрмсдк. h)
description: '\_ \_ \_ Структура сведений о шифровании WMDRM содержит сведения, необходимые для настройки интерфейса ивмдрменкриптскаттер для использования.'
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- Формат WMDRM_ENCRYPT_SCATTER_INFO структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721021"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>\_ \_ \_ Структура сведений о шифровании WMDRM

Структура **\_ \_ \_ сведений о шифровании WMDRM** содержит сведения, необходимые для настройки интерфейса [**ивмдрменкриптскаттер**](iwmdrmencryptscatter.md) для использования.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двстреамид**
</dt> <dd>

Идентификатор потока для шифрования.

</dd> <dt>

**двсамплепротектионверсион**
</dt> <dd>

Пример версии защиты, используемой для кодирования данных из указанного потока.

</dd> <dt>

**кбпротектионинфо**
</dt> <dd>

Размер буфера **пбпротектионинфо** в байтах.

</dd> <dt>

**пбпротектионинфо**
</dt> <dd>

Буфер, содержащий дополнительные сведения о защите.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура используется методом [**ивмдрменкриптскаттер:: инитенкриптскаттер**](iwmdrmencryptscatter-initencryptscatter.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





