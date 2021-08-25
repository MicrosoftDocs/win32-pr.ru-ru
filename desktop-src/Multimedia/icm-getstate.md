---
title: Сообщение ICM_GETSTATE (VFW. h)
description: Сообщение ICM \_ -State запрашивает драйвер сжатия видео, чтобы вернуть его текущую конфигурацию в блок памяти или определить объем памяти, необходимый для получения сведений о конфигурации.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- сообщение ICM_GETSTATE Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bf21d808752b8a3ac3ba71a8593cd6dc577b3af4f34f421682d126c73b3578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784954"
---
# <a name="icm_getstate-message"></a>\_Сообщение о состоянии ICM

Сообщение **ICM- \_ State** запрашивает драйвер сжатия видео, чтобы вернуть его текущую конфигурацию в блок памяти или определить объем памяти, необходимый для получения сведений о конфигурации. Это сообщение можно отправить явно или с помощью макроса [**икжетстате**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*PV*
</dt> <dd>

Указатель на блок памяти, в котором должны содержаться текущие сведения о конфигурации. Можно указать **значение NULL** для этого параметра, чтобы определить объем памяти, необходимый для данных конфигурации, как в [**икжетстатесизе**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Размер блока памяти в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если *ПС* имеет **значение NULL**, возвращает объем памяти в байтах, необходимый для сведений о конфигурации.

Если *ПС* не **равен null**, функция возвращает ицерр \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Структура, используемая для представления сведений о конфигурации, зависит от драйвера и определяется драйвером.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 

 





