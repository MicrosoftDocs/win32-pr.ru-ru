---
description: Указывает, использует ли подсистема захвата ускорение видео DirectX (ДКСВА) для декодирования видео.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Атрибут MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c722b70e1707e6ad5d14b7afca0da2c8d1a63b3a132345e727de1f37023916a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941014"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>\_Ключ записи \_ MF \_ Отключить \_ атрибут дксва

Указывает, использует ли подсистема захвата ускорение видео DirectX (ДКСВА) для декодирования видео.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется, если выполняются следующие условия.

-   Подсистема отслеживания декодирует сжатый поток видео с устройства записи (например, если устройство записи выводит H. 264).
-   Видеодекодер поддерживает декодирование с аппаратным ускорением с помощью ДКСВА.
-   Приложение использует атрибут [ \_ \_ \_ \_ диспетчера D3D подсистемы захвата MF](mf-capture-engine-d3d-manager.md) для установки диспетчер устройств DXGI в подсистеме записи.

В противном случае этот атрибут игнорируется.

Этот атрибут позволяет приложению отключить ДКСВА, продолжая декодироваться на поверхности Direct3D.

Значение этого атрибута по умолчанию равно **false**, означающее, что при наличии включен декодирование дксва.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                         |
| Заголовок<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




