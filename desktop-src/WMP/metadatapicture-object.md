---
title: Объект Метадатапиктуре
description: Объект Метадатапиктуре предоставляет способ получения значений атрибута метаданных WM/Picture. Этот атрибут соответствует обложке альбома, содержащейся в цифровом файле мультимедиа, а не к обложкам альбома, загруженным через Интернет.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Проигрыватель Windows Media Object Метадатапиктуре
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488129"
---
# <a name="metadatapicture-object"></a>Объект Метадатапиктуре

Объект **метадатапиктуре** предоставляет способ получения значений атрибута метаданных [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) . Этот атрибут соответствует обложке альбома, содержащейся в цифровом файле мультимедиа, а не к обложкам альбома, загруженным через Интернет.

Объект **метадатапиктуре** поддерживает следующие свойства:



| Свойство                                           | Описание                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**nописание**](metadatapicture-description.md) | Извлекает описание образа метаданных.    |
| [**Успешности**](metadatapicture-mimetype.md)       | Возвращает тип MIME изображения метаданных.    |
| [**пиктуретипе**](metadatapicture-picturetype.md) | Возвращает тип изображения для метаданных. |
| [**URL-адрес**](metadatapicture-url.md)                 | Только для внутреннего применения.                                |



 

Доступ к объекту **метадатапиктуре** осуществляется с помощью следующего метода.



| Объект                        | Метод                                               |
|-------------------------------|------------------------------------------------------|
| [**Мультимедиа**](media-object.md) | [**жетитеминфобитипе**](media-getiteminfobytype.md) |



 

В целях иллюстрации `player.currentMedia.getItemInfoByType(name, language, index)` используется в разделах синтаксиса Reference.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Справочник по объектной модели для создания сценариев**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 