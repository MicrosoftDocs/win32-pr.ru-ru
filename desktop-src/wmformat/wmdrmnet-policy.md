---
title: Структура WMDRMNET_POLICY (Вмдрмсдк. h)
description: '\_Структура политики вмдрмнет содержит политику, используемую для операций с сетевыми устройствами Windows Media DRM.'
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- Формат WMDRMNET_POLICY структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647959"
---
# <a name="wmdrmnet_policy-structure"></a>\_Структура политики вмдрмнет

Структура **\_ политики вмдрмнет** содержит политику, используемую для операций с сетевыми устройствами Windows Media DRM.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**еполицитипе**
</dt> <dd>

Член перечисления [**\_ \_ типа политики вмдрмнет**](wmdrmnet-policy-type.md) , указывающий тип политики.

</dd> <dt>

**пбполици**
</dt> <dd>

Буфер, содержащий политику. Единственным типом политики, поддерживаемым в настоящее время, является **вмдрмнет \_ Policy \_ Type \_ транскриптплай**. Этот элемент является указателем на структуру **\_ \_ транскриптплай политики вмдрмнет** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура используется в качестве параметра для метода [**ивмдрмнеттрансмиттер:: жетлеафлиценсереспонсе**](iwmdrmnettransmitter-getleaflicenseresponse.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> <dt>

[**\_ \_ глобальные требования политики \_ вмдрмнет**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**\_ \_ Минимальная среда политики \_ вмдрмнет**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**\_транскриптплай политика \_ вмдрмнет**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**\_тип политики \_ вмдрмнет**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





