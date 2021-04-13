---
title: Копирование потоков без распаковки данных
description: Копирование потоков без распаковки данных
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- Windows Media Format SDK, копирование потоков
- Расширенный системный формат (ASF), копирование потоков
- ASF (Расширенный системный формат), копирование потоков
- потоки, копирование без распаковки данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831b85ad431a6c4d3f4255c281d22ca17004674f
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "104412684"
---
# <a name="copying-streams-without-decompressing-the-data"></a>Копирование потоков без распаковки данных

Самый простой и распространенный способ скопировать поток из одного файла в другой — извлечь образцы в их сжатом состоянии, а затем записать их в новый файл без распаковки и повторного сжатия. Примеры, полученные из файла в сжатом состоянии, называются примерами потока, так как они не изменяются из их представления в потоке. Рекомендуется всегда использовать примеры Stream для копирования потоков, так как Распаковка и повторное сжатие данных о степени снижения качества. Если необходимо скопировать поток из распакованных данных, см. раздел [копирование потоков с использованием распакованных образцов](copying-streams-using-decompressed-samples.md).

Можно объединить два или более потока в один поток, используя сжатые образцы, но только в том случае, если скорость потока идентична. Процесс по сути аналогичен описанным ниже действиям, за исключением того, что необходимо прочитать несколько исходных файлов, чтобы получить все необходимое содержимое. Однако сжатые образцы можно записывать только из нескольких файлов в один поток, если структуры **\_ \_ типов мультимедиа WM** (включая все члены структуры **пбформат** ) всех сжатых потоков идентичны. Чтобы объединить данные из нескольких потоков, отформатированных в разных форматах, необходимо распаковать содержимое и повторно сжать его в потоке назначения. Кроме того, при объединении данных из двух или более потоков в один поток необходимо добавить значения окна буфера для всех потоков вместе, чтобы получить окно буфера для нового потока. Это обусловлено тем, что невозможно определить объем буфера, занимаемый в конце одного потока и в начале другого.

Вы можете получить примеры потоков в асинхронном модуле чтения с помощью [**ивмреадерадванцед:: сетрецеивестреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples). Образцы потоков доставляются в [**ивмреадеркаллбаккадванцед:: онстреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample), а не в [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). При чтении файла и извлечении некоторых потоков, сжатых и некоторых распакованных, необходимо реализовать оба метода обратного вызова.

Синхронный модуль чтения обеспечивает большую гибкость при извлечении образцов. Можно свободно переключаться между сжатыми и распакованными примерами при воспроизведении с помощью [**ивмсинкреадер:: сетреадстреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples).

Чтобы скопировать весь поток из одного ASF-файла в новый файл ASF, выполните следующие действия. В этих шагах используется синхронный модуль чтения, так как гораздо проще использовать этот тип операции.

1.  Создайте синхронный объект Reader, вызвав функцию [**вмкреатесинкреадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .
2.  Откройте файл в модуле чтения с помощью вызова [**ивмсинкреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Получите указатель на интерфейс [**ивмпрофиле**](iwmprofile.md) объекта синхронного модуля чтения, вызвав **Ивмсинкреадер:: QueryInterface**.
4.  Получите свойства нужного потока, вызвав [**ивмпрофиле:: жетстреамбинумбер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber). При этом будет получен указатель на интерфейс [**ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) объекта конфигурации потока для нужного потока.
5.  Получение копии структуры [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для потока. Выполните два вызова [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype): First, чтобы получить размер структуры, второй — для получения самой структуры.
6.  Создайте объект диспетчера профилей, вызвав функцию [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
7.  Вызовите [**ивмпрофилеманажер:: креатимптипрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) , чтобы создать новый профиль (или откройте существующий профиль, в который необходимо добавить поток). Вызовите [**ивмпрофиле:: аддстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) в новом профиле, чтобы добавить поток из существующего файла. При добавлении потока используйте указатель **ивмстреамконфиг** , полученный на шаге 4.
8.  Создайте объект модуля записи с помощью вызова функции [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Задайте вновь созданный профиль в качестве активного профиля в модуле записи, вызвав [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Создайте файл для вывода, вызвав [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).
9.  Для каждого входа, связанного с копируемым потоком или потоками, вызовите [**ивмвритер:: сетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops), передав **значение NULL** для интерфейса [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) . Это информирует объект модуля записи о том, что не требуется проверять передаваемые данные. Этот вызов необходимо выполнить перед вызовом **бегинвритинг** (шаг 14). в противном случае объект чтения не сможет декодировать содержимое.
10. Установите синхронное средство чтения для доставки образцов сжатого потока для выбранного потока путем вызова [**ивмсинкреадер:: сетреадстреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) с параметром *фкомпрессед* , установленным в значение true.
11. Получите сведения о кодека для каждого копируемого потока и добавьте сведения о кодека в заголовок перед записью. Чтобы получить сведения о кодека, вызовите [**IWMHeaderInfo2:: жеткодеЦинфокаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) и [**IWMHeaderInfo2:: жеткодеЦинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) , чтобы перечислить кодеки, связанные с файлом, в модуле чтения. Выберите сведения о кодека, соответствующие конфигурации потока. Затем задайте сведения о кодека в средстве записи, вызвав [**IWMHeaderInfo3:: аддкодеЦинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), передав данные, полученные от модуля чтения.
12. Получите указатель на интерфейс [**ивмвритерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) , вызвав **Ивмвритер:: QueryInterface**.
13. Задайте для модуля записи режим записи, вызвав [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
14. Сделайте повторяющиеся вызовы к [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample), указав нужный номер потока. При получении выборок передайте их в модуль записи с помощью вызовов [**ивмвритерадванцед:: вритестреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample). Для видеопотоков следует проверить флаги (если они заданы), заданные модулем записи при каждом вызове **жетнекстсампле**. Если установлено приложение WM \_ SF \_ клеанпоинт, необходимо также задать его при вызове **вритестреамсампле**.
15. По завершении чтения вызовите метод [**ивмвритер:: ендвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting). Поток должен быть передан.

> [!Note]  
> Потоки изображений не могут быть скопированы из одного файла в другой с помощью примеров потока. Чтобы скопировать данные потока изображений, извлеките примеры без сжатия и затем обработайте их через модуль записи, как обычно.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Копирование данных из одного файла в другой**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Копирование потоков с использованием распакованных образцов**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




