---
description: 'Дополнительные сведения: функции API CAB-файла'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Функции API CAB-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b08234a47c84a604c78275632d88be2bcdeef68e47fd092bbf50e4d97dcf925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668358"
---
# <a name="cabinet-api-functions"></a>Функции API CAB-файла

В этом разделе описаны следующие функции API CAB-файлов:

## <a name="fci-functions"></a>Функции FCI

Библиотека FCI (интерфейс сжатия файлов) предоставляет возможность создания ящиков (также называемых CAB-файлами). Кроме того, Библиотека обеспечивает сжатие для уменьшения размера файловых данных, хранящихся в ящиках.



| Компонент                                   | Описание                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**фЦиаддфиле**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Добавляет файл в создается в данный момент.<br/>                                           |
| [**фЦикреате**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Создает контекст FCI.<br/>                                                                          |
| [**фЦидестрой**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Удаляет открытый контекст FCI, освобождая все память и временные файлы, связанные с контекстом.<br/> |
| [**фЦифлушкабинет**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Завершает текущий CAB-файл.<br/>                                                                   |
| [**фЦифлушфолдер**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Принудительное завершение текущей папки в ходе разработки.<br/>                        |



 

## <a name="fdi-functions"></a>Функции FDI

Библиотека FDI (интерфейс распаковки файлов) предоставляет возможность извлечения файлов из ящиков.



| Компонент                                         | Описание                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**фдикопи**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Извлекает файлы из CAB.<br/>                                                          |
| [**фдикреате**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Создает контекст FDI.<br/>                                                                |
| [**фдидестрой**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Удаляет открытый контекст FDI.<br/>                                                           |
| [**фдиискабинет**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Определяет, является ли файл CAB-файлом, и, если он есть, возвращает описательные сведения.<br/> |
| [**фдитрункатекабинет**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Усекает CAB-файл, начиная с указанного номера папки.<br/>                      |



 

## <a name="deprecated-functions"></a>Нерекомендуемые функции

-   [**делетикстрактедфилес**](deleteextractedfiles.md)
-   [**дллжетверсион**](dllgetversion.md)
-   [**Распаковк**](extract.md)
-   [**жетдллверсион**](getdllversion.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по API CAB-файлов](cabinet-api-reference.md)
</dt> <dt>

[Использование API CAB-файла](using-the-cabinet-api.md)
</dt> </dl>

 

 




