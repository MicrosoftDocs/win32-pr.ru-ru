---
title: Метод списка воспроизведения. Мовеитем
description: Метод Мовеитем изменяет расположение элемента в списке воспроизведения.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- Мовеитем метод Windows Media Player
- Мовеитем метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод Мовеитем
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708556"
---
# <a name="playlistmoveitem-method"></a>Метод списка воспроизведения. Мовеитем

Метод **мовеитем** изменяет расположение элемента в списке воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*олдиндекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), содержащее старый индекс.

</dd> <dt>

*невиндекс* \[ окне\]
</dt> <dd>

**Число** (**длинное**), содержащее новый индекс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Списки воспроизведения, хранящиеся в библиотеке, могут изменяться вне элемента управления. Не забудьте отслеживать и обрабатывать все соответствующие события, связанные с списками воспроизведения, чтобы порядок элементов в списке воспроизведения неожиданно изменялся.

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

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





