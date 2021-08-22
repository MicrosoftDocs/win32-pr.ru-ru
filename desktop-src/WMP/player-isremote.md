---
title: Player. Remote
description: свойство "remote" извлекает значение, указывающее, выполняется ли элемент управления проигрыватель Windows Media в удаленном режиме.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Player. remote проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afa0caf615563f4829f1a337f31521b1fb7dafd5ef6e2722f1d50c01dda1ba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616694"
---
# <a name="playerisremote"></a>Player. Remote

свойство " **remote** " извлекает значение, указывающее, выполняется ли элемент управления проигрыватель Windows Media в удаленном режиме.

## <a name="syntax"></a>Синтаксис

*проигрыватель* . **Удаленный**

## <a name="possible-values"></a>Возможные значения

Это свойство является **логическим значением**, доступным только для чтения.



| Значение | Описание                                   |
|-------|-----------------------------------------------|
| Да  | Элемент управления "проигрыватель" работает в удаленном режиме. |
| false | Элемент управления "проигрыватель" выполняется в локальном режиме.  |



 

## <a name="remarks"></a>Remarks

**проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение false.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Реализация удаленного управления проигрывателем Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





