---
title: Медиаколлектион. Жетбяттрибутеандмедиатипе, метод
description: Метод Жетбяттрибутеандмедиатипе извлекает объект списка воспроизведения, содержащий объекты мультимедиа с указанным атрибутом и типом мультимедиа.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- Жетбяттрибутеандмедиатипе метод Windows Media Player
- Жетбяттрибутеандмедиатипе метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетбяттрибутеандмедиатипе
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
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648871"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> </dl>

 

 





