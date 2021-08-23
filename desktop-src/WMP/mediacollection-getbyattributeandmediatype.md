---
title: Медиаколлектион. Жетбяттрибутеандмедиатипе, метод
description: Метод Жетбяттрибутеандмедиатипе извлекает объект списка воспроизведения, содержащий объекты мультимедиа с указанным атрибутом и типом мультимедиа.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- проигрыватель Windows Media метода жетбяттрибутеандмедиатипе
- проигрыватель Windows Media метода жетбяттрибутеандмедиатипе, класс медиаколлектион
- класс медиаколлектион проигрыватель Windows Media, метод жетбяттрибутеандмедиатипе
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46dab1bdcb511e4c96374b17bc6a98be95e48fd64d005eb856c9ec247af48f2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647884"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>Медиаколлектион. Жетбяттрибутеандмедиатипе, метод

Метод **жетбяттрибутеандмедиатипе** извлекает объект **списка воспроизведения** , содержащий объекты **мультимедиа** с указанным атрибутом и типом мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибут* \[ окне\]
</dt> <dd>

**Строка** , содержащая атрибут.

</dd> <dt>

*значение* \[ окне\]
</dt> <dd>

**Строка** , содержащая значение.

</dd> <dt>

*mediaType* \[ окне\]
</dt> <dd>

**Строка** , содержащая тип носителя. Должно содержать одно из следующих значений: "аудио", "видео", "Фото", "список воспроизведения" или "другое".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **списка воспроизведения**

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> </dl>

 

 





