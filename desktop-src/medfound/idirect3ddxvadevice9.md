---
description: Представляет аппаратный ускоритель для ускорения видео DirectX (ДКСВА) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Интерфейс IDirect3DDXVADevice9 (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711791"
---
# <a name="idirect3ddxvadevice9-interface"></a>Интерфейс IDirect3DDXVADevice9

Представляет аппаратный ускоритель для ускорения видео DirectX (ДКСВА) 1,0.

## <a name="members"></a>Элементы

Интерфейс **IDirect3DDXVADevice9** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DDXVADevice9** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IDirect3DDXVADevice9** содержит следующие методы.



| Метод                                                  | Описание                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [**бегинфраме**](idirect3ddxvadevice9-beginframe.md)   | Начинает обработку для создания декодированного изображения.<br/>         |
| [**ендфраме**](idirect3ddxvadevice9-endframe.md)       | Завершает обработку для создания декодированного изображения.<br/>           |
| [**Работать**](idirect3ddxvadevice9-execute.md)         | Выполняет операцию декодирования ДКСВА. <br/>                       |
| [**QueryStatus**](idirect3ddxvadevice9-querystatus.md) | Запрашивает состояние чтения/записи для области декодирования ДКСВА. <br/> |



 

## <a name="remarks"></a>Комментарии

Чтобы получить указатель на этот интерфейс, вызовите метод [**IDirect3DVideoDevice9:: креатедксвадевице**](idirect3dvideodevice9-createdxvadevice.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы видео Direct3D](direct3d-video-interfaces.md)
</dt> </dl>

 

 
