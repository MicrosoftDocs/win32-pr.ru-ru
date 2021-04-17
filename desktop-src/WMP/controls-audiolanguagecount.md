---
title: Controls. Аудиолангуажекаунт
description: Свойство Аудиолангуажекаунт извлекает количество поддерживаемых аудио языков.
ms.assetid: a6dda8bf-db8c-4e97-9277-5a23dfa93156
keywords:
- Проигрыватель Windows Media Controls. Аудиолангуажекаунт
topic_type:
- apiref
api_name:
- Controls.audioLanguageCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09193eb19580d9456f25ea336fe68b8d21e06bae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698798"
---
# <a name="controlsaudiolanguagecount"></a>Controls. Аудиолангуажекаунт

Свойство **аудиолангуажекаунт** извлекает количество поддерживаемых аудио языков.

``` syntax
player.controls.audioLanguageCount
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.

**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Controls. Куррентаудиолангуаже**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. Куррентаудиолангуажеиндекс**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. Жетаудиолангуажедескриптион**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. Жетаудиолангуажеид**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. Жетлангуаженаме**](controls-getlanguagename.md)
</dt> </dl>

 

 





