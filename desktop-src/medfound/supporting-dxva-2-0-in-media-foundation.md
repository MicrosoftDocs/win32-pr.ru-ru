---
description: Поддержка ДКСВА 2,0 в Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Поддержка ДКСВА 2,0 в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170b9c8ccdbdb7e0844b79e5743c4a84b033b7d504378dba083be5adfb244fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721933"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Поддержка ДКСВА 2,0 в Media Foundation

В этом разделе описывается, как поддерживать ускорение видео DirectX (ДКСВА) 2,0 в Media Foundation преобразовании (MFT) с помощью Microsoft Direct3D 9, в частности, описывается взаимодействие между декодером и модулем подготовки видео, который исправляется загрузчиком топологии. В этом разделе не описывается, как реализовать декодирование ДКСВА.

В оставшейся части этого раздела термин *декодера* ОТНОСИТСЯ к MFT декодера, который получает сжатое видео и выводит несжатое видео. Термин *устройство декодера* относится к аппаратному ускорителю, реализованному графическим драйвером.

> [!TIP]
> Сведения о декодировании видео в Microsoft Direct3D 11 см. [в статье поддержка декодирования видео Direct3D 11 в Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Windows Приложения Магазина должны использовать Direct3D 11.

 

Ниже приведены основные шаги, которые должен выполнить декодер для поддержки ДКСВА 2,0 в Media Foundation:

1.  Откройте маркер устройства Direct3D 9.
2.  Найдите конфигурацию декодера ДКСВА.
3.  Выделение несжатых буферов.
4.  Декодирование кадров.

Эти действия более подробно описаны в оставшейся части этого раздела.

## <a name="opening-a-direct3d-device-handle"></a>Открытие обработчика устройства Direct3D

В MFT используется диспетчер устройств Microsoft Direct3D для получения маркера устройства Direct3D 9. Чтобы открыть маркер устройства, выполните следующие действия.

1.  Предоставьте атрибуту [MF \_ SA с \_ \_ поддержкой D3D](mf-sa-d3d-aware-attribute.md) значение **true**. Загрузчик топологии запрашивает этот атрибут путем вызова [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Присвоение атрибуту значения **true** сообщает загрузчику топологии, что MFT поддерживает дксва.
2.  Когда начинается согласование формата, загрузчик топологии вызывает [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) с сообщением из [**таблицы MFT \_ \_ Set D3D Message \_ \_ Manager**](mft-message-set-d3d-manager.md) . Параметр *улпарам* — это указатель **IUnknown** на диспетчер устройств Direct3D модуля подготовки видео. Запросите этот указатель для интерфейса [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Вызовите [**IDirect3DDeviceManager9:: опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) , чтобы получить маркер устройства Direct3D визуализатора.
4.  Вызовите [**IDirect3DDeviceManager9:: жетвидеосервице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) и передайте в него маркер устройства. Этот метод возвращает указатель на интерфейс [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Кэширование указателей и маркера устройства.

## <a name="finding-a-decoder-configuration"></a>Поиск конфигурации декодера

MFT должен найти совместимую конфигурацию для устройства декодера ДКСВА. Выполните следующие действия в методе [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) после проверки входного типа:

1.  Вызовите [**идиректксвидеодекодерсервице:: жетдекодердевицегуидс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Этот метод возвращает массив идентификаторов GUID устройства декодера.
2.  Пройдите по массиву идентификаторов GUID декодера, чтобы найти те, которые поддерживает декодер. Например, для декодера MPEG-2 необходимо найти **DXVA2 \_ ModeMPEG2 \_ мокомп**, **DXVA2 \_ ModeMPEG2 \_ идкт** или **DXVA2 \_ ModeMPEG2 \_ ВЛД**.

3.  При обнаружении идентификатора GUID устройства-кандидата передайте GUID в метод [**идиректксвидеодекодерсервице:: жетдекодеррендертаржетс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Этот метод возвращает массив форматов целевого объекта прорисовки, указанных как значения **D3DFORMAT** .
4.  Пройдите по форматам целевого объекта рендеринга и найдите формат, поддерживаемый декодером.
5.  Вызовите [**идиректксвидеодекодерсервице:: жетдекодерконфигуратионс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Передайте тот же GUID устройства декодера вместе с структурой [**\_ видеодеск DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) , описывающей предложенный выходной формат. Метод возвращает массив структур [**DXVA2 \_ конфигпиктуредекоде**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Каждая структура описывает одну возможную конфигурацию для устройства декодера. Найдите конфигурацию, которую поддерживает декодер.
6.  Сохраните формат целевого объекта прорисовки и конфигурацию.

В методе [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) возвращает несжатый видеоформат на основе предполагаемого формата целевого объекта прорисовки.

В методе [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) Проверьте тип носителя в соответствии с форматом целевого объекта прорисовки.

### <a name="fallback-to-software-decoding"></a>Откат к декодированию программного обеспечения

Если MFT не удается найти конфигурацию ДКСВА (например, если графический драйвер не имеет нужных возможностей), он должен вернуть код ошибки **MF \_ E \_ неподдерживаемый \_ \_ тип D3D** из методов [**сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) и [**сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . Загрузчик топологии будет отвечать, отправляя сообщение [**MFT \_ \_ \_ \_ диспетчера D3D**](mft-message-set-d3d-manager.md) в виде значения **null** для параметра *улпарам* . Таблица MFT должна освободить указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Затем загрузчик топологии повторно согласовывает тип носителя, и MFT может использовать программное декодирование.

## <a name="allocating-uncompressed-buffers"></a>Выделение несжатых буферов

В ДКСВА 2,0 декодер отвечает за выделение поверхностей Direct3D для использования в качестве несжатых буферов видео. Декодер должен выделить 3 поверхности, чтобы Евр использовать для дечередования. Это число является фиксированным, так как Media Foundation не дает возможности Евр указать, сколько поверхностей графический драйвер требует для дечередования. Для любого драйвера должен быть достаточно трех поверхностей.

В методе [**имфтрансформ:: жетаутпутстреаминфо**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) Задайте флаг **\_ \_ \_ \_ Samples в выходной поток** MFT в структуре [**\_ \_ \_ сведений потока вывода MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Этот флаг уведомляет сеанс мультимедиа о том, что MFT выделяет свои собственные выходные примеры.

Чтобы создать поверхности, вызовите метод [**идиректксвидеоакцелератионсервице:: креатесурфаце**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface). (Интерфейс [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) наследует этот метод от [**идиректксвидеоакцелератионсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).) Это можно сделать в [**сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)после поиска формата целевого объекта прорисовки.

Для каждой поверхности вызовите [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) , чтобы создать пример мультимедиа для размещения поверхности. Метод возвращает указатель на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .

## <a name="decoding"></a>Декодирование

Чтобы создать устройство декодера, вызовите метод [**идиректксвидеодекодерсервице:: креатевидеодекодер**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). Метод возвращает указатель на интерфейс [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) устройства декодера.

Декодирование должно происходить внутри метода [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Для проверки маркера устройства в каждом кадре вызовите [**IDirect3DDeviceManager9:: тестдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) . Если устройство изменилось, метод возвращает **DXVA2 \_ E \_ новое \_ видео \_ устройство**. Если это происходит, выполните следующие действия.

1.  Закройте обработчик устройства, вызвав [**IDirect3DDeviceManager9:: клоседевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Освободите указатели [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) и [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Откройте новый маркер устройства.
4.  Согласование новой конфигурации декодера, как описано в разделе "Поиск конфигурации декодера" выше на этой странице.
5.  Создайте новое устройство декодера.

Предполагая, что маркер устройства является допустимым, процесс декодирования работает следующим образом:

1.  Получить доступную поверхность, которая сейчас не используется. (Изначально доступны все поверхности.)
2.  Запросите пример носителя для интерфейса [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Вызовите метод [**имфтраккедсампле:: сеталлокатор**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) и укажите указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , реализованный декодером. Когда модуль подготовки видео освобождает пример, будет вызван обратный вызов декодера.
4.  Вызовите [**идиректксвидеодекодер:: бегинфраме**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
5.  Сделайте следующее или несколько раз:
    1.  Вызовите [**идиректксвидеодекодер::-buffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) , чтобы получить буфер декодера дксва.
    2.  Заполните буфер.
    3.  Вызовите [**идиректксвидеодекодер:: релеасебуффер**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
    4.  Вызовите метод [**идиректксвидеодекодер:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , чтобы выполнить операции декодирования в кадре.

ДКСВА 2,0 использует те же структуры данных, что и ДКСВА 1,0, для операций декодирования. Для исходного набора профилей ДКСВА (для H. 261, H. 263 и MPEG-2) эти структуры данных описаны в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

В каждой паре вызовов [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**выполнения**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) бегинфраме можно вызвать метод несколько [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) раз, но только один раз для каждого типа буфера дксва. Если вызвать его дважды с тем же типом буфера, данные будут перезаписаны.

Используйте обратный вызов из метода [**сеталлокатор**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (шаг 3), чтобы отследить, какие образцы доступны в данный момент и какие используются.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ускорение видео DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
