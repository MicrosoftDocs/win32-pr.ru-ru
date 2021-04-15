---
title: Перечисление WMDRMNET_POLICY_TYPE (Вмдрмсдк. h)
description: '\_ \_ Тип перечисления тип политики вмдрмнет перечисляет типы политик, доступных для операций с сетевыми устройствами Windows Media DRM.'
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- Формат Windows Media WMDRMNET_POLICY_TYPE перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648902"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>\_ \_ Перечисление типов политики вмдрмнет

Тип **перечисления \_ \_ тип политики вмдрмнет** перечисляет типы политик, доступных для операций с сетевыми устройствами Windows Media DRM.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_тип политики вмдрмнет не \_ \_ определен**
</dt> <dd>

Неопределенные типы политик не поддерживаются.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_тип политики \_ вмдрмнет \_ транскриптплай**
</dt> <dd>

Политика управляет возможностью преобразования содержимого, защищенного Windows Media DRM, в защищенный Windows Media DRM для данных сетевых устройств и их воспроизведения на сетевом устройстве.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](drm-enumeration-types.md)
</dt> <dt>

[**\_Политика вмдрмнет**](wmdrmnet-policy.md)
</dt> </dl>

 

 





