---
title: Создание файлов ASF в DirectShow (пакет SDK для формата Windows Media 11)
description: Создание файлов ASF в DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, создание файлов ASF в DirectShow
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный системный формат (ASF), создание в DirectShow
- ASF (Расширенный системный формат), создание в DirectShow
- DirectShow, создание файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134898"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Создание файлов ASF в DirectShow (пакет SDK для формата Windows Media 11)

С помощью DirectShow можно создавать файлы ASF непосредственно из источников захвата, таких как видеокамеры или перекодировать другие файлы в формат Windows Media. В любом сценарии приложения создают графы фильтров, в которых в качестве модуля подготовки отчетов включен фильтр [записи WM ASF](wm-asf-writer-filter.md) .

Модуль записи WM ASF предоставляет частичную оболочку для пакета SDK Windows Media Format. Приложения могут использовать интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) фильтра для передачи системного профиля (версии 4, 7 или 8) или напрямую использовать пакет SDK формата Windows Media для создания настраиваемого профиля для передачи в фильтр. Чтобы добавить метаданные и другие сведения о заголовке, приложение использует интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , который можно получить из фильтра. После настройки профиля и метаданных приложение может просто запустить граф фильтра. На внутреннем уровне фильтр использует пакет SDK Windows Media Format для записи файла. Фильтр обрабатывает все данные синхронизации аудио-видео, которые в противном случае были бы ответственными за приложение.

Этот процесс более подробно описывается в следующих разделах.



| Section                                                                                                           | Описание                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Настройка модуля записи WM ASF (КАСФ)](configuring-the-wm-asf-writer--qasf.md)                                   | Описание настройки фильтра модуля записи WM ASF.                                   |
| [Создание графов фильтров для записи файлов ASF (КАСФ)](building-filter-graphs-to-write-asf-files--qasf.md)           | Описывает, как создавать графы для перекодирования и записи файлов.                           |
| [Настройка профилей и других свойств файлов (КАСФ)](configuring-profiles-and-other-file-properties--qasf.md) | Описывает, как выполнять различные задачи настройки файлов ASF с помощью модуля записи WM ASF. |



 

 

 
