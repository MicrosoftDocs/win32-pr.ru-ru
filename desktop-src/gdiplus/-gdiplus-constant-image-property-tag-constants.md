---
description: Несколько форматов файлов изображений позволяют хранить метаданные вместе с изображением.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Константы тега свойства Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509caf20659628909d225bb2dc34a4dbaa27047c08e361b28e9777141f213751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696422"
---
# <a name="image-property-tag-constants"></a>Константы тега свойства Image

Несколько форматов файлов изображений позволяют хранить метаданные вместе с изображением. Метаданные — это сведения о изображении, например заголовок, ширина, модель камеры и исполнитель. Windows GDI+ предоставляет единообразный способ хранения и извлечения метаданных из файлов изображений в формате TIFF, JPEG, png и файлов обмена изображениями (EXIF).

в GDI+ часть метаданных называется *элементом свойства*, а отдельный элемент свойства идентифицируется с помощью числовой константы, называемой *тегом свойства*. Метаданные можно хранить и извлекать путем вызова методов [**Image:: сетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) и [**Image:: жетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , и вам не нужно беспокоиться о том, как конкретный формат файлов сохраняет эти метаданные.

В следующих разделах перечислены и описаны элементы свойств, поддерживаемые GDI+. Описания являются краткими и общими, поэтому они применяются к различным форматам файлов. Подробное описание использования элемента свойства в определенном формате файла см. в спецификации для этого формата файла. Ссылки на несколько спецификаций формата файла см. в разделе [спецификации формата файла изображения](-gdiplus-constant-image-file-format-specifications.md). Дополнительные сведения о метаданных см. в разделе [чтение и запись метаданных](-gdiplus-reading-and-writing-metadata-use.md) и [**констант типа тега свойства Image**](-gdiplus-constant-image-property-tag-type-constants.md).

-   [Теги свойств в числовом порядке](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Теги свойств в алфавитном порядке](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Описания элементов свойств](-gdiplus-constant-property-item-descriptions.md)

 

 



