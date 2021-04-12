---
title: Сообщение MCIWNDM_GETDEVICE (VFW. h)
description: Сообщение МЦИВНДМing \_ возвращает имя текущего открытого устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетдевице.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489426"
---
# <a name="mciwndm_getdevice-message"></a>\_Сообщение мЦивндм

Сообщение **мЦивндмing \_** возвращает имя текущего открытого устройства MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетдевице**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*len*
</dt> <dd>

Размер буфера в байтах.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Указатель на определенный приложением буфер для возврата имени устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ненулевое значение в противном случае.

## <a name="remarks"></a>Комментарии

Если строка, заканчивающаяся символом NULL, содержащая имя устройства, длиннее, чем буфер, МЦивнд усекает его.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





