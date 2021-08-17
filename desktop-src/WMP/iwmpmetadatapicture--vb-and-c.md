---
title: Интерфейс Ивмпметадатапиктуре (VB и C) (WMP. h)
description: Предоставляет свойства для получения сведений об образе, содержащемуся в цифровом файле мультимедиа, представленном атрибутом WM/Пиктуреметадата.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- проигрыватель Windows Media интерфейса ивмпметадатапиктуре (VB и C)
- проигрыватель Windows Media интерфейса ивмпметадатапиктуре (VB и C), описание
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b73a48b2ea93d696f2b8780edec90dfcf0522e2353c508e31d96dd7a404d0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996494"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>Интерфейс Ивмпметадатапиктуре (VB и C#)

Предоставляет свойства для получения сведений об образе, содержащемуся в цифровом файле мультимедиа, представленном атрибутом метаданных [**WM/Picture**](/windows/desktop/wmformat/wmpicture). Этот атрибут соответствует изображениям альбома, содержащимся в цифровом файле мультимедиа, а не к обложкам альбома, загруженным через Интернет.

Интерфейс **ивмпметадатапиктуре** предоставляет следующие свойства.



| Свойство                                                                                   | Описание                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Описание**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Возвращает описание изображения, представленного атрибутом метаданных.  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Возвращает тип MIME изображения, представленного атрибутом метаданных.    |
| [**пиктуретипе**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Возвращает тип изображения, представленного атрибутом метаданных. |
| [**URL-адрес**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | Только для внутреннего применения.                                                        |



 

Получите интерфейс **ивмпметадатапиктуре** , передав имя атрибута [**WM/Picture**](/windows/desktop/wmformat/wmpicture) следующему методу и приведя возвращаемый объект.



| Интерфейс                                  | Свойство                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**жетитеминфобитипе**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Элементы

Интерфейс **ивмпметадатапиктуре (VB и C#)** не определяет никаких членов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**интерфейсы для Visual Basic .net и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

