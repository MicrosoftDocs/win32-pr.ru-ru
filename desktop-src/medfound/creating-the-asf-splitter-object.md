---
description: Создание объекта разделителя ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Создание объекта разделителя ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5782f42b53607943704836c350b76e69d872e8d9654959d4453d8e029c21f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600814"
---
# <a name="creating-the-asf-splitter-object"></a>Создание объекта разделителя ASF

Объект- *Разделитель* ASF — это объект слоя вмконтаинер, который анализирует объект данных ASF в файле ASF. Чтобы создать новый экземпляр объекта разделителя ASF, вызовите функцию [**мфкреатеасфсплиттер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) . Эта функция возвращает указатель на интерфейс [**имфасфсплиттер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) , представляющий пустой объект-разделитель.

Прежде чем разделитель может начать анализ, приложение должно инициализировать разделитель данными из объекта заголовка ASF. Чтобы инициализировать разделитель, вызовите метод [**имфасфсплиттер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) . Этот метод принимает указатель на [объект ASF контентинфо](asf-contentinfo-object.md) , который содержит сведения о заголовке ASF-файла для синтаксического анализа. Приложение должно инициализировать объект Контентинфо перед передачей его в разделитель, чтобы характеристики файла мультимедиа были известны приложению. Метод **Initialize** разделителя извлекает сведения о потоке из объекта контентинфо, например номера потоков, поэтому разделитель может проанализировать пакеты данных.

### <a name="example"></a>Пример

В следующем примере кода показано, как создать разделитель и инициализировать его с помощью существующего объекта Контентинфо.


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> В этом примере функция [саферелеасе](saferelease.md) используется для высвобождения указателей интерфейса.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разделитель ASF](asf-splitter.md)
</dt> </dl>

 

 



