---
title: Метод списка воспроизведения. insertItem
description: Метод insertItem вставляет элемент мультимедиа в список воспроизведения в указанном расположении.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- insertItem метод Windows Media Player
- insertItem метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704130"
---
# <a name="playlistinsertitem-method"></a>Метод списка воспроизведения. insertItem

Метод **insertItem** вставляет элемент мультимедиа в список воспроизведения в указанном расположении.

## <a name="syntax"></a>Синтаксис


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), содержащее индекс, по которому нужно добавить элемент.

</dd> <dt>

*элемент* \[ окне\]
</dt> <dd>

Вставляемый объект **мультимедиа** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Номера индексов всех элементов после вставленного элемента будут увеличены на единицу.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Список воспроизведения. элемент**](playlist-item.md)
</dt> <dt>

[**Список воспроизведения. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





