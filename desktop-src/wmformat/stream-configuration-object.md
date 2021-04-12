---
title: Объект конфигурации потока
description: Объект конфигурации потока
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media Format SDK, объекты конфигурации потока
- Расширенный системный формат (ASF), объекты конфигурации потока
- ASF (Расширенный системный формат), объекты конфигурации потока
- объекты, объекты конфигурации Stream
- объекты конфигурации потока
- потоки, объекты конфигурации потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104133582"
---
# <a name="stream-configuration-object"></a>Объект конфигурации потока

Объект конфигурации потока используется для указания свойств потока мультимедиа в файле ASF. Объекты конфигурации потока могут быть созданы для существующих потоков в профиле или могут быть созданы пустыми и готовы к получению новых данных. Объекты конфигурации потока не могут существовать независимо от объекта профиля. Чтобы сохранить содержимое объекта конфигурации потока, необходимо вызвать метод [**ивмпрофиле:: аддстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) , чтобы добавить новый поток или [**Ивмпрофиле:: реконфигстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) для сохранения изменений, внесенных в существующий поток.

Чтобы создать объект конфигурации потока, используйте один из следующих методов.



| Метод                                                                | Описание                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Ивмпрофиле:: Креатеневстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Создает объект конфигурации потока без каких-либо данных.                                                                          |
| [**Ивмпрофиле:: Stream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Создает объект конфигурации потока, заполненный данными из профиля. Использует индекс потока для задания нужного потока.  |
| [**Ивмпрофиле:: Жетстреамбинумбер**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Создает объект конфигурации потока, заполненный данными из профиля. Использует номер потока для задания нужного потока. |



 

Все методы в приведенной выше таблице устанавливают указатель на интерфейс **ивмстреамконфиг** . Другие интерфейсы объекта конфигурации потока можно получить, вызвав метод **QueryInterface** .

Объект конфигурации Stream поддерживает следующие интерфейсы.



| Интерфейс                                        | Описание                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ивммедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Задает и получает структуру [**\_ \_ типа WM Media**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для потока.                                    |
| [**ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Задает и получает свойства, которые не требуются для всех потоков, например для параметров переменной скорости (VBR).                  |
| [**ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Задает и извлекает все основные сведения о потоке.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Настраивает типы модулей обработки данных, связанных с потоком. Наследует все методы **ивмстреамконфиг**. |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Задает и получает язык для потока. Наследует все методы **ивмстреамконфиг** и **IWMStreamConfig2**. |
| [**ивмвидеомедиапропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Управляет свойствами потока видео. Это необязательный интерфейс, который доступен только для потоков видео.            |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Настройка потоков**](configuring-streams.md)
</dt> <dt>

[**Объекты**](objects.md)
</dt> <dt>

[**Объект диспетчера профилей**](profile-manager-object.md)
</dt> </dl>

 

 




