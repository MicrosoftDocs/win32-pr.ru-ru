---
description: Создание экземпляра кодека МФТС
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Создание экземпляра кодека МФТС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263174"
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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Работа с кодеками МФТС](workingwithcodecmfts.md)
</dt> </dl>

 

 
