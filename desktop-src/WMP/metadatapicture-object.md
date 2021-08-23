---
title: Объект Метадатапиктуре
description: Объект Метадатапиктуре предоставляет способ получения значений атрибута метаданных WM/Picture. Этот атрибут соответствует обложке альбома, содержащейся в цифровом файле мультимедиа, а не к обложкам альбома, загруженным через Интернет.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- проигрыватель Windows Media объекта метадатапиктуре
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 261ed17a156e1b5563b52744490e2ed014803eb9f1e75c182f44d5bd228b11c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996214"
---
# <a name="metadatapicture-object"></a>Объект Метадатапиктуре

Объект **метадатапиктуре** предоставляет способ получения значений атрибута метаданных [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) . Этот атрибут соответствует обложке альбома, содержащейся в цифровом файле мультимедиа, а не к обложкам альбома, загруженным через Интернет.

Объект **метадатапиктуре** поддерживает следующие свойства:



| Свойство                                           | Описание                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**nописание**](metadatapicture-description.md) | Извлекает описание образа метаданных.    |
| [**mimeType**](metadatapicture-mimetype.md)       | Возвращает тип MIME изображения метаданных.    |
| [**пиктуретипе**](metadatapicture-picturetype.md) | Возвращает тип изображения для метаданных. |
| [**URL-адрес**](metadatapicture-url.md)                 | Только для внутреннего применения.                                |



 

Доступ к объекту **метадатапиктуре** осуществляется с помощью следующего метода.



| Объект                        | Метод                                               |
|-------------------------------|------------------------------------------------------|
| [**Носитель**](media-object.md) | [**жетитеминфобитипе**](media-getiteminfobytype.md) |



 

В целях иллюстрации `player.currentMedia.getItemInfoByType(name, language, index)` используется в разделах синтаксиса Reference.

## <a name="see-also"></a>См. также

<dl> <dt>

[**Справочник по объектной модели для создания сценариев**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 