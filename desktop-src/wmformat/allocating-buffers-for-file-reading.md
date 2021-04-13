---
title: Выделение буферов для чтения файлов
description: Выделение буферов для чтения файлов
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media Format SDK, чтение файлов ASF
- Расширенный формат систем (ASF), чтение файлов
- ASF (Расширенный системный формат), чтение файлов
- Windows Media Format SDK, выделение буферов
- Расширенный системный формат (ASF), выделение буферов
- ASF (Расширенный системный формат), выделение буферов
- Расширенный системный формат (ASF), выделение буфера
- ASF (Расширенный системный формат), выделение буфера
- выделение буфера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412473"
---
# <a name="allocating-buffers-for-file-reading"></a>Выделение буферов для чтения файлов

В самом базовом сценарии чтения файлов буферы, используемые для доставки образцов, выделяются объектом чтения (объектом Reader или синхронным объектом Reader). Однако можно самостоятельно выделить буферы. Дополнительные сведения о преимуществах выделения собственных буферов см. в разделе [Поддержка выводимых пользователем примеров](user-allocated-sample-support.md).

Чтобы использовать собственные буферы для чтения файлов, выполните следующие действия.

1.  Реализуйте обратный вызов или обратные вызовы, чтобы средство чтения вызывало, когда требуется буфер. При чтении выходных образцов используйте [**ивмреадераллокаторекс:: аллокатефораутпутекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex). При чтении образцов потоков используйте [**ивмреадераллокаторекс:: аллокатефорстреамекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex). Включите любую логику для управления буферами, которые подходят для вашего приложения.
2.  Выделите пул буферов, которые будут использоваться для чтения файлов.
    -   Определите размер, необходимый для буферов, вызвав [**ивмреадерадванцед:: жетмаксаутпутсамплесизе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) или [**Ивмреадерадванцед:: жетмаксстреамсамплесизе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) для каждого выхода и (или) потока, для которого используется буфер. При использовании синхронного модуля чтения используйте вместо него [**ивмсинкреадер:: жетмаксаутпутсамплесизе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) или [**Ивмсинкреадер:: жетмаксстреамсамплесизе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) .
    -   Создайте каждый буфер для пула.
3.  Настройка модуля чтения или синхронного модуля чтения для чтения. Дополнительные сведения см. в статье [чтение файлов с помощью асинхронного модуля чтения](reading-files-with-the-asynchronous-reader.md) или [чтение файлов с помощью синхронного модуля чтения](reading-files-with-the-synchronous-reader.md).
4.  Прежде чем начать запись, вызовите [**ивмреадерадванцед:: сеталлокатефораутпут**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) или [**Ивмреадерадванцед:: сеталлокатефорстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) для каждого выхода и потока, для которого производится выделение буферов с помощью объекта Reader. Для синхронного модуля чтения вызовите метод [**IWMSyncReader2:: сеталлокатефораутпут**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) или [**IWMSyncReader2:: сеталлокатефорстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) .
5.  Начните чтение файла.

Объект чтения будет вызывать соответствующий обратный вызов распределителя и получать примеры из приложения. Логика управления буфером должна включать способ сигнализации о том, что буфер может быть снова использован. Как правило, буфер помещается обратно в пул, когда его содержимое готовится к просмотру. В зависимости от приложения может потребоваться всего несколько буферов в пуле или многие из них.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Чтение файлов ASF**](reading-asf-files.md)
</dt> </dl>

 

 




