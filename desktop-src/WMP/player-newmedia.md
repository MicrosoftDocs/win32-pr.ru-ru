---
title: Метод Player. Невмедиа
description: Метод Невмедиа создает новый объект мультимедиа.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- проигрыватель Windows Media метода невмедиа
- метод невмедиа проигрыватель Windows Media, класс Player
- класс Player проигрыватель Windows Media, метод невмедиа
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e3ad30db7ec43bcc0ee6c1470dc608ccf1625390486d9fcd0fd4bf018affdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338109"
---
# <a name="playernewmedia-method"></a>Метод Player. Невмедиа

Метод **невмедиа** создает новый объект **мультимедиа** .

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*URL-адрес* \[ окне\]
</dt> <dd>

**Строка** , содержащая URL-адрес файла цифрового мультимедиа, с которым создается объект **мультимедиа** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **мультимедиа** .

## <a name="remarks"></a>Remarks

Параметр *URL-адреса* не должен быть пустой строкой или иметь значение null.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





