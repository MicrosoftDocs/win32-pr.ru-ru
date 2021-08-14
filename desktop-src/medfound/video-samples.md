---
description: Образцы видео
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Образцы видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3883b3a62cd907c89dd46d14681e28ad9a4d4d94653a9f04a9097707d22cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972603"
---
# <a name="video-samples"></a>Образцы видео

Пример объекта Video — это Специализированная реализация интерфейса [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) для использования с расширенным модулем [подготовки видео](enhanced-video-renderer.md) (Евр). Чтобы создать экземпляр этого объекта, вызовите функцию [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) . Функция принимает указатель на поверхность Direct3D и возвращает указатель на интерфейс **имфсампле** . Следующие типы объектов должны выделять примеры с помощью этой функции:

-   Пользовательские Выступающие Евр. Выступающие выделяют видеоролики и отправляет их в метод микшера [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Дополнительные сведения см. [в разделе как написать Евр Presenter](how-to-write-an-evr-presenter.md).

-   Видеодекодеры, поддерживающие ускорение видео. Дополнительные сведения см. [в разделе Поддержка дксва 2,0 в Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

Пример объекта Video реализует следующие интерфейсы:

-   [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**имфдесиредсампле**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Если параметр *пунксурфаце* объекта [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) имеет значение, отличное от **null**, то результирующий пример видео содержит один буфер мультимедиа, который инкапсулирует поверхность Direct3D. Этот Буферный объект имеет ограниченную функциональность:

-   Метод [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) буфера возвращает E \_ нотимпл.

-   В буфере не реализован интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .

Единственный способ получить доступ к поверхности из буфера — вызвать [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), используя идентификатор службы MR \_ buffer \_ .

Если параметр *пунксурфаце* имеет **значение NULL**, пример видео создается с нулевыми буферами носителей. Чтобы добавить буфер в образец, выполните следующие действия.

1.  Создайте поверхность Direct3D.

2.  Создайте буфер Surface, вызвав [**мфкреатедкссурфацебуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer). Дополнительные сведения см. в разделе [буфер поверхности DirectX](directx-surface-buffer.md).

3.  Добавьте буфер в образец, вызвав [**имфсампле:: аддбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Используйте этот подход, если требуется доступ к памяти поверхности через интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Буферы мультимедиа](media-buffers.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> </dl>

 

 
