---
title: Плайлистаррай. Item, метод
description: Метод Item извлекает список воспроизведения по указанному индексу.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- проигрыватель Windows Media метода элемента
- метод item проигрыватель Windows Media, класс плайлистаррай
- класс плайлистаррай проигрыватель Windows Media, метод item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a45bb38250285563d9e4b7abcc1a4bfd1f7a0bea35b41b7e4cd801f8eff1d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335431"
---
# <a name="playlistarrayitem-method"></a>Плайлистаррай. Item, метод

Метод **Item** извлекает список воспроизведения по указанному индексу.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**длинное**), содержащее индекс списка воспроизведения, который требуется получить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **списка воспроизведения** .

## <a name="remarks"></a>Remarks

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Плайлистаррай**](playlistarray-object.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





