---
title: Использование файловых приемников
description: Использование файловых приемников
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Расширенный формат систем (ASF), приемники файлов
- ASF (Расширенный системный формат), приемники файлов
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- приемники, приемники файлов
- приемники файлов, сведения
- приемники файлов, создание
- приемники файлов, остановка
- приемники файлов, запуск
- приемники файлов, закрытие
- приемники, статистика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104133578"
---
# <a name="using-file-sinks"></a>Использование файловых приемников

В обычных обстоятельствах можно просто передать имя выходного файла с помощью метода [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) , и объект модуля записи автоматически запишет файл на диск. В этом случае модуль записи фактически создает и управляет объектом приемника файла модуля записи, который обрабатывает запись файла на диск. Объект приемника файла модуля записи управляет потоком данных из объекта модуля записи в один файл.

Можно создать собственные приемники файлов, чтобы получить больший контроль над тем, как приемник записывает файл. Кроме того, можно получить доступ к приемнику файла модуля записи по умолчанию, созданному модулем записи в ответ на вызов **сетаутпутфиленаме**.

## <a name="creating-file-sinks"></a>Создание приемников файлов

Чтобы создать приемник файла и добавить его в модуль записи, выполните следующие действия.

1.  Создайте новый приемник, вызвав функцию [**вмкреатевритерфилесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .
2.  Укажите имя файла для приемника, вызвав [**ивмвритерфилесинк:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).
3.  Добавьте приемник файла в модуль записи, вызвав [**ивмвритерадванцед:: аддсинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).
4.  Выполните написание обычным способом.
5.  После завершения записи приемник закроет файл автоматически.

## <a name="stopping-and-starting-file-sinks"></a>Остановка и запуск приемников файлов

После начала записи можно прерывать в приемнике файлов, вызвав [**IWMWriterFileSink2:: останавливаться**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).

Существует множество потенциальных причин, по которым вы захотите прерывать запись в приемник. Например, если вы записываете данные из активного источника, вы можете заинтересовать только часть содержимого.

Вы можете возобновить запись в приемник файлов, вызвав [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start). И **останавливают** , и **начинают** использовать время презентации для управления приблизительно при выполнении команды. Методы [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) можно использовать для получения большего контроля над временем начала и окончания.

## <a name="closing-file-sinks"></a>Закрытие приемников файлов

Как правило, приемник файла закрывается автоматически. Если запись в приемник закончена, но операции записи в другие приемники продолжаются, необходимо явным образом закрыть приемник для экономии ресурсов. Чтобы закрыть приемник файла, вызовите метод [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Получение статистики приемника

Можно получить размер и длительность файла для открытого приемника, вызвав [**IWMWriterFileSink2:: GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) и [**IWMWriterFileSink2:: жетфиледуратион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) соответственно.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмвритерфилесинк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**Интерфейс IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**Интерфейс IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Объект приемника файлов модуля записи**](writer-file-sink-object.md)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 




