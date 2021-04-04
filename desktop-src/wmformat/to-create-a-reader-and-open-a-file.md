---
title: Создание средства чтения и открытие файла
description: Создание средства чтения и открытие файла
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Расширенный системный формат (ASF), создание читателей
- ASF (Расширенный системный формат), создание читателей
- Расширенный формат систем (ASF), открытие файлов
- ASF (Расширенный системный формат), открытие файлов
- асинхронные читатели, создание
- асинхронные читатели, открытие файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789216"
---
# <a name="to-create-a-reader-and-open-a-file"></a>Создание средства чтения и открытие файла

Прежде чем выполнять какие-либо действия с модулем чтения, необходимо создать объект Reader и загрузить файл для чтения. Чтобы инициализировать средство чтения и открыть файл, выполните следующие действия.

1.  Создайте объект Reader, вызвав функцию [**вмкреатереадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) . Необходимо указать требуемый уровень Rights Management для нового объекта модуля чтения. Доступные режимы перечислены в типе перечисления [**\_ Rights ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .
2.  Укажите файл для чтения путем вызова [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open). Необходимо указать интерфейс обратного вызова модуля чтения, который будет использоваться средством чтения. Дополнительные сведения о обратном вызове модуля чтения см. в разделе [Реализация сообщений модуля чтения в обратном вызове OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).
3.  Дождитесь открытия файла средством чтения. При вызове метода **Open** для загрузки файла он сразу же возвращается и возобновляет обработку в другом потоке. Дождитесь завершения операций, получив событие, когда обратный вызов **OnStatus** получает \_ сообщение о состоянии ВМТ Opened.

Модуль чтения также поддерживает использование интерфейса **IStream** com для открытия файлов. Интерфейс **IStream** можно реализовать любым выбранным способом. После открытия требуемого файла в **IStream** можно выполнить приведенные выше действия, за исключением того, что необходимо вызвать [**IWMReaderAdvanced2:: опенстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) вместо **ивмреадер:: Open** на шаге 2.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Интерфейс IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Интерфейс Ивмстатускаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[**Чтение файлов с помощью асинхронного модуля чтения**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Использование методов обратного вызова**](using-the-callback-methods.md)
</dt> </dl>

 

 




