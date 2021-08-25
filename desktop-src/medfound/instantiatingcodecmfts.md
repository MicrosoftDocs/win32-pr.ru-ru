---
description: Создание экземпляра кодека МФТС
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Создание экземпляра кодека МФТС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73af4055aee1d5b7e6a3ea137ab2204c9e59194f57ae4776e6c8368429db877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827614"
---
# <a name="instantiating-codec-mfts"></a>Создание экземпляра кодека МФТС

[Media Foundation преобразования](media-foundation-transforms.md) (МФТС) — это COM-объекты, реализующие интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . MFT — это объект для преобразования мультимедийных данных в составе конвейера. Конвейер — это направленный ациклический граф, состоящий из источников мультимедиа, преобразований мультимедиа и приемников мультимедиа. Конвейер обрабатывает потоковые данные мультимедиа в асинхронном режиме.

Несмотря на то, что МФТС можно создавать и использовать независимо от Media Foundation инфраструктуры конвейера, предпочтительнее использовать платформу Медиафаундатион, где это возможно.

Можно создать MFT кодека, вызвав функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . Необходимо передать идентификатор класса MFT, идентификатор интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)и указатель на указатель **имфтрансформ** .

Идентификаторы класса кодека МФТС определены как константы в файле заголовка вмкодекдсп. h.

Константа для идентификатора интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) — IID \_ имфтрансформ.

В следующем примере кода показано, как создать экземпляр MFT кодека:


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Работа с кодеками МФТС](workingwithcodecmfts.md)
</dt> </dl>

 

 
