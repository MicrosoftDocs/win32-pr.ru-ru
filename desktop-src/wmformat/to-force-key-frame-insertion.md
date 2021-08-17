---
title: Принудительная Вставка Key-Frame
description: Принудительная Вставка Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Расширенный системный формат (ASF), принудительная вставка ключевых кадров
- ASF (Расширенный системный формат), принудительная вставка ключевых кадров
- Расширенный формат систем (ASF), вставка ключевых кадров
- ASF (Расширенный системный формат), вставка ключевых кадров
- ключевые кадры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d400c0ee4ba97aa7de559b1394dbe5c9fb2a974c124924aeae0839b1b4dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196500"
---
# <a name="to-force-key-frame-insertion"></a>Принудительная Вставка Key-Frame

кодек Windows Media Video 9 поддерживает принудительную вставку по ключевым кадрам. При передаче образца в модуль записи можно указать, что он должен быть закодирован в виде [*ключевого кадра*](wmformat-glossary.md).

Чтобы принудительно вставить ключевые кадры для примера, выполните следующие действия.

1.  Выделите буфер для хранения образца и получите указатель на интерфейс [**инссбуффер**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) , содержащий буфер, вызвав [**Ивмвритер:: аллокатесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Извлеките расположение и размер буфера, созданного на шаге 1, вызвав [**инссбуффер:: жетбуфферандленгс**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).
3.  Скопируйте образец данных в буферное расположение, убедившись, что переданный образец будет помещаться в выделенный буфер. В зависимости от источника выборки можно использовать различные функции для копирования данных. Например, при копировании потока из AVI-файла можно использовать функцию AVI **авистреамреад**.
4.  Обновите объем данных, используемых в буфере, чтобы отразить фактический размер образца путем вызова [**инссбуффер:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Получите указатель на интерфейс [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) , вызвав **Инссбуффер:: QueryInterface**.
6.  Задайте пример в качестве принудительного ключевого кадра, вызвав метод [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) , чтобы установить \_ свойство WM сампликстенсионгуид \_ аутпутклеанпоинт. Это свойство имеет логическое значение. Задайте для него **значение true**.
7.  Передайте интерфейс буфера записи, а также входной номер и время выборки с помощью метода [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Ивмвритер:: Вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**Написание образцов**](to-write-samples.md)
</dt> <dt>

[**Кодирование переменной скорости (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 




