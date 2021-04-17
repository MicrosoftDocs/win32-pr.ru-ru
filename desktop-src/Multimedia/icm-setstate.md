---
title: Сообщение ICM_SETSTATE (VFW. h)
description: Сообщение ICM \_ SETSTATE уведомляет драйверу о сжатии видео о необходимости установки состояния сжатия. Это сообщение можно отправить явно или с помощью макроса Иксетстате.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672927"
---
# <a name="icm_setstate-message"></a>\_Сообщение ICM SETSTATE

Сообщение **ICM \_ SETSTATE** уведомляет драйверу о сжатии видео о необходимости установки состояния сжатия. Это сообщение можно отправить явно или с помощью макроса [**иксетстате**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*PV*
</dt> <dd>

Указатель на блок памяти, содержащий данные конфигурации. Можно указать **значение NULL** для этого параметра, чтобы сбросить сжатие до состояния по умолчанию.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Размер блока памяти в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число байтов, используемых модулем сжатия в случае успешного или нулевого значения.

## <a name="remarks"></a>Комментарии

Сведения, используемые этим сообщением, являются частными и относятся к конкретному компрессору. Клиентские приложения должны использовать это сообщение только для восстановления сведений, ранее полученных с помощью сообщения [**ICM- \_ State**](icm-getstate.md) , и должны использовать параметр [**ICM \_ Configure**](icm-configure.md) для настройки драйвера сжатия видео.

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

 

 





