---
description: В этом разделе описывается реализация преобразования Media Foundation с поддержкой Direct3D (MFT) для видео.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware МФТС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae3bc071ee707505fd7412cba6f0a5aa397fd4c3f623225da28cc5490bf3323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958743"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware МФТС

В этом разделе описывается реализация преобразования Media Foundation с *поддержкой Direct3D* (MFT) для видео.

Видеофайл MFT считается *совместимым с Direct3D* , если он может обрабатывать образцы, содержащие поверхности Direct3D. Типичная причина поддержки Direct3D в видеофайловых ТАБЛИЦАх — включение декодирования с аппаратным ускорением с использованием ускорения DirectX Video (ДКСВА).

В этом разделе описаны шаги, необходимые для создания MFT-совместимого с Direct3D. В этом разделе не рассматривается механизм декодирования ДКСВА. Дополнительные сведения о ДКСВА см. в статье [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md).

> [!IMPORTANT]
> начиная с Windows 8 можно использовать [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) вместо [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). для приложений магазина Windows необходимо использовать **имфдксгидевицеманажер** и Microsoft Direct3D 11. Дополнительные сведения см. в статье [API-интерфейсы видео Direct3D 11](direct3d-11-video-apis.md).

 

1.  Реализуйте метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Этот метод возвращает указатель на хранилище атрибутов.
2.  MFT должно установить значение **true** для атрибута [**MF \_ SA с \_ \_ поддержкой D3D**](mf-sa-d3d-aware-attribute.md) в собственном хранилище атрибутов. начиная с Windows 8, при использовании Direct3D 11 используйте [ \_ \_ \_ уведомления MF SA D3D11](mf-sa-d3d11-aware.md).
3.  Во время согласования формата, если атрибут [**MF \_ SA \_ \_**](mf-sa-d3d-aware-attribute.md) (или [MF \_ SA \_ D3D11, \_ осведомленный](mf-sa-d3d11-aware.md) об использовании Direct3D 11) имеет **значение true**, клиент может отправить в основную таблицу MFT сообщение из [**таблицы MFT \_ \_ Set D3D Message \_ \_ Manager**](mft-message-set-d3d-manager.md) . Параметр события *улпарам* является указателем на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . начиная с Windows 8 можно использовать [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) вместо **IDirect3DDeviceManager9**. Клиенту не требуется отсылать это сообщение.
4.  MFT вызывает [**IDirect3DDeviceManager9:: жетвидеосервице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) для запроса необходимых служб дксва. начиная с Windows 8, если используется [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) , то MFT вызывает [**имфдксгидевицеманажер:: жетвидеосервице**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Обычно декодер запрашивает [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice), а обработчик видео запрашивает [**идиректксвидеопроцессорсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice).
5.  При условии успешного выполнения предыдущего шага методы [**имфтрансформ:: жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) и [**Имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) должны возвращать дксва совместимые форматы.
6.  Клиент настраивает типы носителей в MFT. Если тип мультимедиа несовместим с ДКСВА, MFT должен вернуть код ошибки **MF \_ E \_ неподдерживаемый \_ \_ тип D3D**.
7.  На этом этапе есть два варианта, в зависимости от того, находит ли клиент подходящий формат ДКСВА.
    -   Если клиент успешно настроил формат ДКСВА, он может начать обработку. На этом этапе MFT может использовать ДКСВА для обработки или вернуться к обработке программного обеспечения.
    -   Кроме того, если клиент не находит приемлемый формат ДКСВА, клиент может отправить еще одно сообщение [**MFT \_ \_ Manager Set \_ D3D \_**](mft-message-set-d3d-manager.md) Message, при этом параметру *улпарам* будет присвоено **значение NULL**. MFT должен освободить указатель [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) (указатель [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) , если использовался **ИМФДКСГИДЕВИЦЕМАНАЖЕР** ) и другие интерфейсы дксва, а также вернуться к обработке программного обеспечения. На этом этапе MFT не должно использовать обработку ДКСВА.

Таблица MFT, поддерживающая Direct3D, должна быть подготовлена к обработке образцов, содержащих поверхность Direct3D. Пример будет содержать ровно один буфер мультимедиа. Чтобы получить поверхность Direct3D из буфера, вызовите функцию [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) и укажите службу **\_ \_ службы буфера MR** . Дополнительные сведения см. в разделе [буфер поверхности DirectX](directx-surface-buffer.md).

Файл MFT, использующий ДКСВА, должен выделить свои собственные выходные примеры следующим образом:

1.  В методе [**имфтрансформ:: жетаутпутстреаминфо**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) Задайте флаг **\_ \_ \_ \_ Samples в потоке вывода MFT** .
2.  Создайте пул поверхностей ДКСВА, как описано в спецификации ДКСВА.
3.  Создайте примеры носителей, вызвав [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface).

MFT всегда должно поддерживать обработку программного обеспечения в качестве резерва, так как обработка ДКСВА может быть недоступна по нескольким причинам:

-   GPU может не поддерживать ДКСВА.
-   Клиент может не использовать Direct3D.
-   Профили ДКСВА не определяются для каждого видеоформата.

Файловая таблица, поддерживающая Direct3D, должна иметь один выходной поток. Он не может иметь несколько выходов.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запись пользовательского MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



