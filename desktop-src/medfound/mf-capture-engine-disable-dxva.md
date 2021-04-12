---
description: Указывает, использует ли подсистема захвата ускорение видео DirectX (ДКСВА) для декодирования видео.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Атрибут MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343935"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>\_Ключ записи \_ MF \_ Отключить \_ атрибут дксва

Указывает, использует ли подсистема захвата ускорение видео DirectX (ДКСВА) для декодирования видео.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется, если выполняются следующие условия.

-   Подсистема отслеживания декодирует сжатый поток видео с устройства записи (например, если устройство записи выводит H. 264).
-   Видеодекодер поддерживает декодирование с аппаратным ускорением с помощью ДКСВА.
-   Приложение использует атрибут [ \_ \_ \_ \_ диспетчера D3D подсистемы захвата MF](mf-capture-engine-d3d-manager.md) для установки диспетчер устройств DXGI в подсистеме записи.

В противном случае этот атрибут игнорируется.

Этот атрибут позволяет приложению отключить ДКСВА, продолжая декодироваться на поверхности Direct3D.

Значение этого атрибута по умолчанию равно **false**, означающее, что при наличии включен декодирование дксва.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




