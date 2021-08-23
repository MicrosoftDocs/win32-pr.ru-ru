---
title: Функции пакета SDK Windows Media Format
description: Функции
ms.assetid: 10fa8f96-8030-4727-af5d-7c06229d05d8
keywords:
- Windows Пакет SDK для формата мультимедиа, функции
- Расширенный системный формат (ASF), функции
- ASF (Расширенный системный формат), функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560756451ee2f5b49d26b5611b38a40a45cac7643b101fdbe8ae492386901689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708264"
---
# <a name="windows-media-format-sdk-functions"></a>Функции пакета SDK Windows Media Format

пакет SDK для Windows Media Format включает функции для создания объектов и вспомогательные функции для упрощения некоторых процедур.

Этот пакет SDK поддерживает следующие функции для первоначального создания объектов. Если объект отсутствует в списке ниже, его необходимо создать с помощью интерфейса из другого объекта. Дополнительные сведения см. в статье [Объекты и свойства визуальных элементов Power BI](objects.md).



| Функция                                                                             | Описание                                                                                                                                             |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**вмчеккурлекстенсион**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)                                   | Проверяет расширение имени файла по URL-адресу или имени файла, переданного в качестве аргумента                                                               |
| [**вмчеккурлсчеме**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)                                         | Проверяет сетевой протокол и сравнивает его со внутренним списком поддерживаемых схем.                                                                    |
| [**вмкреатебаккупресторер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                             | Создает объект резервного хранилища архивации.                                                                                                                       |
| [**вмкреатецертификате**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))                                   | Заключает сертификаты пользователя в объект.                                                                                                           |
| [**вмкреатедевицерегистратион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)                     | Создает объект регистрации устройства.                                                                                                                   |
| [**вмкреатедрмтранскриптор**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)                           | Создает объект перешифрования DRM.                                                                                                                      |
| [**вмкреатидитор**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                             | Создает объект редактора метаданных.                                                                                                                       |
| [**вмкреатеиндексер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                                           | Создает объект индексатора.                                                                                                                              |
| [**вмкреателиценсеревокатионажент**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent)             | Создает объект агента отзыва лицензий.                                                                                                              |
| [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                             | Создает объект диспетчера профилей.                                                                                                                       |
| [**вмкреатереадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                             | Создает объект модуля чтения.                                                                                                                                |
| [**вмкреатесекуречаннел**](/previous-versions/windows/desktop/api/Wmsecure/nf-wmsecure-wmcreatesecurechannel)                               | Создает объект, реализующий [**ивмсекуречаннел**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**\_Сертифицированный вмкреатесекуречаннел**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified)          | Создает объект, реализующий [**ивмсекуречаннел**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**Вмкреатесекуречаннел \_ Certified \_ des**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified_des) | Создает объект, реализующий [**ивмсекуречаннел**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                        |
| [**Вмкреатесекуречаннел \_ des**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_des)                      | Создает объект, реализующий [**ивмсекуречаннел**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**вмкреатесинкреадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                                     | Создает синхронный объект Reader.                                                                                                                    |
| [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                             | Создает объект модуля записи.                                                                                                                                |
| [**вмкреатевритерфилесинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                             | Создает объект приемника файла модуля записи.                                                                                                                      |
| [**вмкреатевритернетворксинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)                       | Создает объект сетевого приемника модуля записи.                                                                                                                   |
| [**вмкреатевритерпушсинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                             | Создает объект приемника push-уведомлений.                                                                                                                      |
| [**вмисаваилаблеоффлине**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline)                                 | Проверяет, можно ли воспроизвести файл ASF из кэшированной копии.                                                                                             |
| [**вмисконтентпротектед**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)                                 | Проверяет файл на наличие содержимого, защищенного DRM.                                                                                                                |
| [**вмвалидатедата**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)                                             | проверяет, соответствуют ли данные, начиная с начала файла, с разделом заголовка типа файла, поддерживаемого пакетом SDK для Windows Media Format. |



 

Следующие функции предоставляют удобные сочетания клавиш для анализа файлов.



| Функция                                             | Описание                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**вмчеккурлекстенсион**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)   | пытается определить, доступен ли файл для чтения объектами Windows пакета SDK формата мультимедиа на основе расширения имени файла.              |
| [**вмчеккурлсчеме**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)         | определяет, поддерживается ли сетевой протокол объектами пакета SDK Windows Media Format.                                           |
| [**вмисаваилаблеоффлине**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline) | Определяет, доступен ли файл для автономного воспроизведения.                                                                                 |
| [**вмисконтентпротектед**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected) | Проверяет файл на наличие содержимого, защищенного DRM.                                                                                                     |
| [**вмвалидатедата**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)             | пытается определить, доступен ли файл для чтения объектами пакета SDK Windows Media Format, анализируя данные в начале файла. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Объекты**](objects.md)
</dt> <dt>

[**Справочник по программированию**](programming-reference.md)
</dt> </dl>

 

 
