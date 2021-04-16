---
title: Сообщение MCIWNDM_CHANGESTYLES (VFW. h)
description: Сообщение МЦИВНДМ \_ чанжестилес изменяет стили, используемые в окне мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндчанжестилес.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650366"
---
# <a name="mciwndm_changestyles-message"></a>\_Сообщение мЦивндм чанжестилес

Сообщение **мЦивндм \_ чанжестилес** изменяет стили, используемые в окне мЦивнд. Это сообщение можно отправить явно или с помощью макроса [**мЦивндчанжестилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*виде*
</dt> <dd>

Маска, определяющая стили, которые могут изменяться. Эта маска является побитовым оператором или для всех стилей, которые разрешено изменять.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*значений*
</dt> <dd>

Новые параметры стиля для окна. Укажите ноль для этого параметра, чтобы отключить все стили, определенные в маске. Список доступных стилей см. в разделе Функция [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**мЦивндчанжестилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





