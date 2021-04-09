---
title: Сообщение ICM_GETSTATE (VFW. h)
description: Сообщение ICM \_ -State запрашивает драйвер сжатия видео, чтобы вернуть его текущую конфигурацию в блок памяти или определить объем памяти, необходимый для получения сведений о конфигурации.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE сообщения Windows мультимедиа
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
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137811"
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

## <a name="remarks"></a>Комментарии

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

 

 





