---
description: Включает аппаратное ускорение декодирования устройства Direct3D 9 с помощью ускорения видео DirectX (ДКСВА) версии 1,0.
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Интерфейс IDirect3DVideoDevice9 (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155186"
---
# <a name="idirect3dvideodevice9-interface"></a>Интерфейс IDirect3DVideoDevice9

Включает аппаратное ускорение декодирования устройства Direct3D 9 с помощью ускорения видео DirectX (ДКСВА) версии 1,0.

## <a name="when-to-use"></a>Назначение

Этот интерфейс не предназначен для общего использования приложением. Фильтры декодера DirectShow должны использовать интерфейс [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , а не **IDirect3DVideoDevice9**. Входные контакты фильтра формирователя микширования видео (VMR) и фильтра микшера наложения предоставляют **иамвидеоакцелератор**.

## <a name="members"></a>Элементы

Интерфейс **IDirect3DVideoDevice9** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DVideoDevice9** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IDirect3DVideoDevice9** содержит следующие методы.



| Метод                                                                                   | Описание                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**креатедксвадевице**](idirect3dvideodevice9-createdxvadevice.md)                       | Создает устройство декодера ДКСВА.<br/>                                                                                         |
| [**креатесурфаце**](idirect3dvideodevice9-createsurface.md)                             | Создает сжатую поверхность для декодирования ДКСВА.<br/>                                                                        |
| [**жетдксвакомпресседбуфферинфо**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | Возвращает сведения о сжатых буферах, необходимых для декодирования с аппаратным ускорением.<br/>                                |
| [**жетдксвагуидс**](idirect3dvideodevice9-getdxvaguids.md)                               | Возвращает список профилей ДКСВА, поддерживаемых драйвером экрана.<br/>                                             |
| [**жетдксваинтерналинфо**](idirect3dvideodevice9-getdxvainternalinfo.md)                 | Запрашивает объем вспомогательной памяти, выделяемой слоем абстрагирования оборудования (HAL) для частного использования. <br/> |
| [**жетункомпресседдксваформатс**](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | Возвращает список несжатых форматов пикселей, которые могут быть отображены с помощью указанного профиля ДКСВА.<br/>                         |



 

## <a name="remarks"></a>Комментарии

Чтобы получить указатель на этот интерфейс, вызовите метод **QueryInterface** для указателя [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) или [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .

Этот интерфейс поддерживает только ДКСВА 1,0. Он не поддерживает ДКСВА 2,0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы видео Direct3D](direct3d-video-interfaces.md)
</dt> <dt>

[Ускорение видео DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Спецификация ДКСВА 1,0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
