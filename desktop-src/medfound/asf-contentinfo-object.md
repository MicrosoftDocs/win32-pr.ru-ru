---
description: Объект Контентинфо ASF
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Объект Контентинфо ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692093"
---
# <a name="asf-contentinfo-object"></a>Объект Контентинфо ASF

Объект ASF *контентинфо* сохраняет информацию из объекта заголовка ASF файла. Приложение может использовать объект Контентинфо в следующих целях:

-   Считывает объект заголовка для существующего файла мультимедиа. В этом случае объект Контентинфо анализирует объект заголовка и сохраняет сведения о файле характеристик. Media Foundation предоставляет некоторые из этих свойств через атрибуты и интерфейсы. Они описаны в разделе [атрибуты Media Foundation для объектов заголовка ASF](media-foundation-attributes-for-asf-header-objects.md).
-   Запись данных заголовка и создание объекта заголовка для нового файла.
-   При чтении или записи файла мультимедиа инициализируйте другие объекты ASF, такие как [Разделитель ASF](asf-splitter.md), [мультиплексор ASF](asf-multiplexer.md)и индексатор ASF.

Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).

## <a name="creating-the-contentinfo-object"></a>Создание объекта Контентинфо

Чтобы создать новый экземпляр объекта Контентинфо, вызовите функцию [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) . Этот метод возвращает указатель на пустой объект Контентинфо, который должен быть инициализирован для работы с определенным файлом ASF. В зависимости от того, считывает ли приложение существующий файл или записывает новый ASF-файл, он должен вызвать [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) или [**Имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) для заполнения пустого объекта.

Дополнительные сведения об этих вызовах методов см. в следующих разделах:

-   [Чтение объекта заголовка ASF существующего файла](reading-the-asf-header-object-of-an-existing-file.md)
-   [Получение сведений из объектов заголовка ASF](getting-information-from-asf-header-objects.md)
-   [Запись объекта заголовка ASF для нового файла](writing-an-asf-header-object-for-a-new-file.md)
-   [Атрибуты Media Foundation для объектов заголовка ASF](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Компоненты ASF Вмконтаинер](wmcontainer-asf-components.md)
</dt> </dl>

 

 



