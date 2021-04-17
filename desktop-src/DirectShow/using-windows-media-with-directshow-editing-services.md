---
description: Использование Windows Media с службами редактирования DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Использование Windows Media с службами редактирования DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674527"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>Использование Windows Media с службами редактирования DirectShow

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

В этом разделе описывается использование содержимого на основе Windows Media в приложении [служб редактирования DirectShow](directshow-editing-services.md) (DES). Существует два основных сценария.

-   Исходные клипы. Проект DES может содержать аудио-и видеоклипы из файлов Windows Media.
-   Конечный формат. Windows Media — идеальный формат для окончательных выходных данных проекта редактирования видео.

Для работы с файлами Windows Media приложение должно предоставить сертификат программного обеспечения, который также называется ключом. Для этого реализуется объект поставщика ключа. Поставщик ключей — это COM-объект, предоставляющий интерфейс **IServiceProvider** . Сведения о реализации поставщика ключей см. в разделе [разблокировка пакета SDK Windows Media Format](unlocking-the-windows-media-format-sdk.md).

Чтобы использовать DES с файлами Windows Media, для следующих объектов DES требуется программный ключ:

-   Модуль подготовки отчетов для предварительного просмотра или записи файлов.
-   Объект Медиадет для получения видеокадров или типов мультимедиа из файлов ASF.
-   \[! Существенно\]  
    > Не используйте интеллектуальный модуль визуализации для чтения или записи файлов Windows Media. Всегда используйте базовый механизм визуализации (CLSID \_ рендеренгине).

     

Чтобы предоставить объекту программный ключ, запросите этот объект для интерфейса **IObjectWithSite** и вызовите **IObjectWithSite:: SetSite** с указателем на ваш поставщик ключей. Например, следующий код предоставляет программный ключ модулю визуализации:


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



Чтобы использовать клипы источника Windows Media в проекте DES, просто вызовите **IObjectWithSite:: SetSite** в подсистеме визуализации с указателем на ваш поставщик ключей.

Сведения о создании файлов Windows Media см. [в разделе запись файла Windows Media в Des](writing-a-windows-media-file-in-des.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование служб редактирования DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



