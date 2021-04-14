---
title: Объект (пакет SDK Windows Media Format 11)
description: Объекты
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- Windows Media Format SDK, объекты
- Расширенный системный формат (ASF), объекты
- ASF (Расширенный системный формат), объекты
- объекты, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d73672891395d6491009e1c62fac1f9eb81dfe
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414645"
---
# <a name="objects-windows-media-format-11-sdk"></a>Объект (пакет SDK Windows Media Format 11)

Пакет SDK для формата Windows Media использует несколько объектов для чтения, записи, редактирования и индексирования файлов ASF, а также для создания и изменения профилей. Каждый объект поддерживает ряд интерфейсов. Некоторые интерфейсы поддерживаются в нескольких объектах. В этих случаях все различия в реализации обсуждаются в разделе справки по интерфейсу.

Объекты в пакете SDK формата Windows Media совместимы с COM. Чтобы упростить разработку, каждый объект имеет связанную функцию создания или метод. Объекты следует создавать с помощью функции создания или метода, а не вручную с помощью функции COM **CoCreateInstance**.

К именам некоторых интерфейсов добавляется число, например **IWMProfile2** и **IWMWriter3**. В каждом случае пронумерованные версии наследуют все методы более ранних версий и добавляют новые функциональные возможности.

На каждой странице объектов этой ссылки сначала перечисляются интерфейсы, включенные в основной COM-объект, а затем — интерфейсы обратного вызова, которые должны быть реализованы в приложении.

В следующей таблице перечислены объекты, поддерживаемые этим пакетом SDK, а также описание функций каждой из них и функция, используемая для ее создания.



| Объект                                                          | Описание                                                                                                                                              | Функция создания                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Резервное хранилище архивации](backup-restorer-object.md)                   | Резервное копирование лицензий, обычно на съемные носители, а затем восстановление этих лицензий на другой компьютер.                                           | [**вмкреатебаккупресторер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [Регистрация устройства](device-registration-object.md)           | Управляет базой данных регистрации устройств, которая содержит записи для устройств воспроизведения мультимедиа, доступных через сетевое подключение.             | [**вмкреатедевицерегистратион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [Перешифрованный DRM](drm-transcryptor-object.md)                 | Преобразует данные мультимедиа, защищенные с помощью DRM, в поток данных, который может быть отправлен на устройства, использующие протокол Windows Media DRM 10 для сетевых устройств. | [**вмкреатедрмтранскриптор**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [Индексатор](indexer-object.md)                                   | Создает индекс для файлов ASF, позволяющих выполнять поиск в файлах с помощью видеопотоков.                                                                            | [**вмкреатеиндексер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [Агент отзыва лицензий](license-revocation-agent-object.md) | Управляет отзывом лицензий.                                                                                                                              | [**вмкреателиценсеревокатионажент**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [Редактор метаданных](metadata-editor-object.md)                   | Изменяет метаданные в заголовке файла ASF.                                                                                                                    | [**вмкреатидитор**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [Диспетчер профилей](profile-manager-object.md)                   | Предоставляет интерфейсы для создания, загрузки и сохранения профилей. Для записи ASF-файла необходим профиль.                                                      | [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [Читатель](reader-object.md)                                     | Считывает файлы ASF. Этот объект использует модель асинхронного вызова для своих операций.                                                                      | [**вмкреатереадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [Синхронное средство чтения](synchronous-reader-object.md)             | Считывает файлы ASF с помощью синхронных вызовов.                                                                                                                 | [**вмкреатесинкреадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [Средство](writer-object.md)                                     | Записывает файлы ASF.                                                                                                                                        | [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [Приемник файла модуля записи](writer-file-sink-object.md)                 | Управляет файлами ASF, записанными объектом модуля записи.                                                                                                         | [**вмкреатевритерфилесинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [Приемник сети модуля записи](writer-network-sink-object.md)           | Управляет динамической потоковой передачей файлов ASF, записанных объектом модуля записи.                                                                               | [**вмкреатевритернетворксинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [Приемник push-уведомлений](writer-push-sink-object.md)                 | Управляет доставкой потокового содержимого на серверы публикации.                                                                                            | [**вмкреатевритерпушсинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

В следующей таблице перечислены объекты, зависящие от других объектов. Эти объекты создаются методами существующих объектов.



| Объект                                                        | Описание                                                                                                                                                                                                                                                                                                                           | Метод создания                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Совместное использование пропускной способности](bandwidth-sharing-object.md)             | Управление информацией о совместном использовании пропускной способности в профиле. Для профиля может существовать несколько объектов совместного использования пропускной способности. Существуют различные методы создания объекта для совместной пропускной способности в зависимости от того, нужно ли создать новый объект для совместной использования пропускной способности или получить доступ к существующему объекту.                                           | [**IWMProfile3:: креатеневбандвидсшаринг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) НИ<br/> [**IWMProfile3:: Жетбандвидсшаринг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Буфер](buffer-object.md)                                   | Содержит пример носителя и все связанные с ним расширения модулей данных. Используется как для написания, так и для чтения образцов.                                                                                                                                                                                                                           | [**Ивмвритер:: аллокатесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) НИ<br/> [**Ивмреадераллокаторекс:: Аллокатефораутпутекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> OR<br/> [**Ивмреадераллокаторекс:: Аллокатефорстреамекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> OR<br/> Автоматически создается объектом Reader или синхронным объектом Reader для примера доставки.<br/> |
| [Свойства входного носителя](input-media-properties-object.md)   | Управляет свойствами входных данных. Для каждого входного объекта может существовать один объект входных свойств.                                                                                                                                                                                                                                             | [**Ивмвритер:: Жетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [Взаимное исключение](mutual-exclusion-object.md)               | Управляет взаимоисключающими сведениями в профиле. Распространенные способы взаимного исключения — это многоразрядное содержимое и звуковые дорожки на нескольких языках. Существуют различные методы создания взаимоисключающих объектов в зависимости от того, нужно ли создать новый объект взаимного исключения или получить доступ к существующему.         | [**Ивмпрофиле:: креатеневмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) НИ<br/> [**Ивмпрофиле:: Жетмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [Свойства выходного носителя](output-media-properties-object.md) | Управляет свойствами выходных данных. Для каждого выхода может существовать один объект свойств выходного носителя. Эти объекты могут создаваться модулем чтения или синхронным модулем чтения.                                                                                                                                                            | [**Ивмреадер:: жетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) НИ<br/> [**Ивмсинкреадер:: Жетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [Профиль](profile-object.md)                                 | Содержит данные в профиле, пока выполняется обработка. Объекты профиля создаются каждый раз, когда необходимо управлять профилем. Существует несколько способов создания объекта профиля в зависимости от того, нужно ли создать новый профиль или получить доступ к существующему.                                                  | [**Ивмпрофилеманажер:: креатимптипрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) НИ<br/> [**Ивмпрофилеманажер:: Лоадпрофилебидата**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> OR<br/> [**Ивмпрофилеманажер:: Лоадпрофилебид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> OR<br/> [**Ивмпрофилеманажер:: Лоадсистемпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [Настройка потока](stream-configuration-object.md)       | Управляет свойствами потока в профиле. Объекты конфигурации потока создаются объектами потока каждый раз, когда необходимо получить доступ к сведениям о потоке. Существуют различные методы создания объекта конфигурации потока в зависимости от того, требуется ли создать новый поток или доступ к нему и существующий. | [**Ивмпрофиле:: креатеневстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) НИ<br/> [**Ивмпрофиле:: Stream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> OR<br/> [**Ивмпрофиле:: Жетстреамбинумбер**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [Определение приоритетов потоков](stream-prioritization-object.md)     | Поддерживает список приоритетов потоков для профиля. Потоки будут удалены в порядке возрастания приоритета, если доступная пропускная способность ограничена. В профиле может быть только один объект приоритета потока.                                                                                                                  | [**IWMProfile3:: Креатеневстреамприоритизатион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Справочник по программированию**](programming-reference.md)
</dt> </dl>

 

 





