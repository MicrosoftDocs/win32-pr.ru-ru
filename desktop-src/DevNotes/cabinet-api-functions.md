---
description: 'Дополнительные сведения: функции API CAB-файла'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Функции API CAB-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895678"
---
# <a name="cabinet-api-functions"></a>Функции API CAB-файла

В этом разделе описаны следующие функции API CAB-файлов:

## <a name="fci-functions"></a>Функции FCI

Библиотека FCI (интерфейс сжатия файлов) предоставляет возможность создания ящиков (также называемых CAB-файлами). Кроме того, Библиотека обеспечивает сжатие для уменьшения размера файловых данных, хранящихся в ящиках.



| Функция                                   | Описание                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**фЦиаддфиле**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Добавляет файл в создается в данный момент.<br/>                                           |
| [**фЦикреате**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Создает контекст FCI.<br/>                                                                          |
| [**фЦидестрой**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Удаляет открытый контекст FCI, освобождая все память и временные файлы, связанные с контекстом.<br/> |
| [**фЦифлушкабинет**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Завершает текущий CAB-файл.<br/>                                                                   |
| [**фЦифлушфолдер**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Принудительное завершение текущей папки в ходе разработки.<br/>                        |



 

## <a name="fdi-functions"></a>Функции FDI

Библиотека FDI (интерфейс распаковки файлов) предоставляет возможность извлечения файлов из ящиков.



| Функция                                         | Описание                                                                                       |
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по API CAB-файлов](cabinet-api-reference.md)
</dt> <dt>

[Использование API CAB-файла](using-the-cabinet-api.md)
</dt> </dl>

 

 




