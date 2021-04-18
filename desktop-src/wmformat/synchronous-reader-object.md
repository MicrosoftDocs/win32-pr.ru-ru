---
title: Объект модуля синхронного чтения
description: Объект модуля синхронного чтения
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Пакет SDK для формата Windows Media, синхронные объекты чтения
- Расширенный формат систем (ASF), синхронные объекты чтения
- ASF (Расширенный системный формат), синхронные объекты чтения
- объекты, синхронные объекты чтения
- синхронные читатели, объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105700824"
---
# <a name="synchronous-reader-object"></a>Объект модуля синхронного чтения

Синхронный объект Reader используется для чтения цифровых файлов мультимедиа с помощью синхронных вызовов.

Синхронный объект Reader создается функцией [**вмкреатесинкреадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), которая устанавливает указатель на интерфейс **ивмсинкреадер** . Другие интерфейсы, поддерживаемые синхронным интерфейсом чтения, можно получить, вызвав метод **QueryInterface** .

Объект синхронного модуля чтения поддерживает следующие интерфейсы.



| Интерфейс                                | Описание                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Задает и получает сведения о заголовке, такие как метаданные, [*маркеры*](wmformat-glossary.md)и т. д.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Перечисляет сведения о доступных кодеках. Наследует все методы **ивмхеадеринфо**.                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Поддерживает крупные размеры атрибутов, дублирующиеся имена атрибутов и поддержку нескольких языков. Наследует все методы **ивмхеадеринфо** и **IWMHeaderInfo2**. |
| [**ивмпрофиле**](iwmprofile.md)         | Предоставляет доступ к сведениям о профиле файла Windows Media, загруженного в средство чтения.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Возвращает глобальный уникальный идентификатор (GUID), если таковой имеется, связанный с профилем. Наследует все методы **ивмпрофиле**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Поддерживает совместное использование пропускной способности и сведения о приоритизации потоков в профиле. Наследует все методы **ивмпрофиле** и **IWMProfile2**.                |
| [**ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Предоставляет возможности синхронного чтения для цифровых файлов мультимедиа.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Обеспечивает поддержку поиска для SMPTE кодов времени и для выделения образцов вручную. Наследует все методы **ивмсинкреадер**.                            |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Объекты**](objects.md)
</dt> <dt>

[**Объект модуля чтения**](reader-object.md)
</dt> <dt>

[**Чтение файлов с помощью синхронного модуля чтения**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




