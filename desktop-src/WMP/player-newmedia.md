---
title: Метод Player. Невмедиа
description: Метод Невмедиа создает новый объект мультимедиа.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- Невмедиа метод Windows Media Player
- метод Невмедиа проигрывателя Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Невмедиа
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
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708519"
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

## <a name="remarks"></a>Комментарии

Параметр *URL-адреса* не должен быть пустой строкой или иметь значение null.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





