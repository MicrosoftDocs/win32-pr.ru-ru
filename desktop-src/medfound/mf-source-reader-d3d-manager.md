---
description: Содержит указатель на диспетчер устройств Microsoft Direct3D для модуля чтения исходного кода.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: Атрибут MF_SOURCE_READER_D3D_MANAGER (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910196"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a>\_ \_ \_ Атрибут диспетчера D3D чтения источника MF \_

Содержит указатель на [Диспетчер устройств Microsoft Direct3D](direct3d-device-manager.md) для [модуля чтения исходного кода](source-reader.md).

## <a name="data-type"></a>Тип данных

**IDirect3DDeviceManager9 \* или имфдксгидевицеманажер \*** хранятся как **IUnknown \** _

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Комментарии

Значение этого атрибута может быть указателем на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) или [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).

Используйте этот атрибут, чтобы предоставить устройство Direct3D для видеодекодеров, загруженных модулем чтения исходного кода. Если установить этот атрибут и декодер поддерживает ускорение видео Microsoft DirectX (ДКСВА), модуль чтения исходного кода использует устройство Direct3D для выделения буферов видео. Эти буферы совместимы с обработчиком видео ДКСВА 2. (См. раздел [Обработка видео дксва](dxva-video-processing.md).)

Используйте этот атрибут со следующими функциями:

-   [**мфкреатесаурцереадерфромбитестреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Обычно этот атрибут задается, если вы используете модуль чтения исходного кода для получения раскодированных видеокадров и используете Direct3D для вывода кадров. Установка этого атрибута позволяет декодеру использовать ДКСВА.

Этот атрибут не задается, если:

-   Модуль чтения исходного кода используется только для обработки аудио и не видео.
-   Вы получаете сжатое видео из модуля чтения исходного кода. В этом случае модуль чтения исходного кода не создает декодер.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Модуль чтения исходного кода](source-reader.md)
</dt> <dt>

[Атрибуты модуля чтения исходного кода](source-reader-attributes.md)
</dt> </dl>

 

 




