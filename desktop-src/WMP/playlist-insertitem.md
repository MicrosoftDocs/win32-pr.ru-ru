---
title: Метод списка воспроизведения. insertItem
description: Метод insertItem вставляет элемент мультимедиа в список воспроизведения в указанном расположении.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- проигрыватель Windows Media метода insertItem
- проигрыватель Windows Media метода insertItem, класс списка воспроизведения
- класс списка воспроизведения проигрыватель Windows Media, метод insertItem
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
ms.openlocfilehash: 7a71d9ceb39b29c1627ea7596166c39b3dc2f6c76faf45e5ffb54bea14154ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995704"
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

## <a name="remarks"></a>Remarks

Номера индексов всех элементов после вставленного элемента будут увеличены на единицу.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Список воспроизведения. элемент**](playlist-item.md)
</dt> <dt>

[**Список воспроизведения. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





