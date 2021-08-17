---
title: Объект модуля синхронного чтения
description: Объект модуля синхронного чтения
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Пакет SDK для формата мультимедиа, синхронные объекты чтения
- Расширенный формат систем (ASF), синхронные объекты чтения
- ASF (Расширенный системный формат), синхронные объекты чтения
- объекты, синхронные объекты чтения
- синхронные читатели, объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 629f08684f996a611acaf00b913eaa8715869bdfd0219ea27994e2f8faf7c896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197064"
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
| [**ивмпрофиле**](iwmprofile.md)         | предоставляет доступ к сведениям о профиле Windowsного файла мультимедиа, загруженного в средство чтения.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Возвращает глобальный уникальный идентификатор (GUID), если таковой имеется, связанный с профилем. Наследует все методы **ивмпрофиле**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Поддерживает совместное использование пропускной способности и сведения о приоритизации потоков в профиле. Наследует все методы **ивмпрофиле** и **IWMProfile2**.                |
| [**ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Предоставляет возможности синхронного чтения для цифровых файлов мультимедиа.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Обеспечивает поддержку поиска для SMPTE кодов времени и для выделения образцов вручную. Наследует все методы **ивмсинкреадер**.                            |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Объекты**](objects.md)
</dt> <dt>

[**Объект модуля чтения**](reader-object.md)
</dt> <dt>

[**Чтение файлов с помощью синхронного модуля чтения**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




