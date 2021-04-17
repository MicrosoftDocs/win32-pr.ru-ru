---
description: Атрибуты потока байтов
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Атрибуты потока байтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692087"
---
# <a name="byte-stream-attributes"></a>Атрибуты потока байтов

Следующие атрибуты применяются к некоторым потокам байтов. Чтобы узнать, поддерживает ли байтовый поток атрибуты, запросите объект потока байтов для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| attribute                                                                                  | Описание                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**\_ \_ тип содержимого MF \_ BYTESTREAM**](mf-bytestream-content-type-attribute.md)              | Указывает тип MIME потока байтов.                         |
| [**\_Длительность BYTESTREAM \_ MF**](mf-bytestream-duration-attribute.md)                       | Задает длительность потока байтов в единицах 100-наносекундных. |
| [\_ \_ \_ URI файла ИФО BYTESTREAM \_](mf-bytestream-ifo-file-uri.md)                           | Указывает URL-адрес связанного файла ИФО.                      |
| [**MF \_ BYTESTREAM \_ \_ время последнего изменения \_**](mf-bytestream-last-modified-time-attribute.md) | Указывает, когда байтовый поток был изменен в последний раз.                   |
| [**\_ \_ имя источника MF \_ BYTESTREAM**](mf-bytestream-origin-name-attribute.md)                | Задает исходный URL-адрес для потока байтов.                     |



 

Следующие атрибуты применяются к обработчикам потока байтов.



| attribute                                                                                    | Описание                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ битестреамхандлер \_ принимает \_ общий доступ к \_ записи](mf-bytestreamhandler-accepts-share-write.md) | Указывает, может ли обработчик потока байтов использовать поток байтов, Открытый для записи другим потоком. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



