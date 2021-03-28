---
description: Несколько форматов файлов изображений позволяют хранить метаданные вместе с изображением.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Константы тега свойства Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985204"
---
# <a name="image-property-tag-constants"></a>Константы тега свойства Image

Несколько форматов файлов изображений позволяют хранить метаданные вместе с изображением. Метаданные — это сведения о изображении, например заголовок, ширина, модель камеры и исполнитель. Windows GDI+ обеспечивает единообразный способ хранения и извлечения метаданных из файлов изображений в формате TIFF, JPEG, PNG и файлов обмена изображениями (EXIF).

В GDI+ фрагмент метаданных называется *элементом свойства*, а отдельный элемент свойства идентифицируется с помощью числовой константы, называемой *тегом свойства*. Метаданные можно хранить и извлекать путем вызова методов [**Image:: сетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) и [**Image:: жетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , и вам не нужно беспокоиться о том, как конкретный формат файлов сохраняет эти метаданные.

В следующих разделах перечислены и описаны элементы свойств, поддерживаемые GDI+. Описания являются краткими и общими, поэтому они применяются к различным форматам файлов. Подробное описание использования элемента свойства в определенном формате файла см. в спецификации для этого формата файла. Ссылки на несколько спецификаций формата файла см. в разделе [спецификации формата файла изображения](-gdiplus-constant-image-file-format-specifications.md). Дополнительные сведения о метаданных см. в разделе [чтение и запись метаданных](-gdiplus-reading-and-writing-metadata-use.md) и [**констант типа тега свойства Image**](-gdiplus-constant-image-property-tag-type-constants.md).

-   [Теги свойств в числовом порядке](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Теги свойств в алфавитном порядке](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Описания элементов свойств](-gdiplus-constant-property-item-descriptions.md)

 

 



