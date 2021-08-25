---
title: Сообщение MCIWNDM_SETREPEAT (VFW. h)
description: Сообщение МЦИВНДМ \_ сетрепеат устанавливает флаг повтора, связанный с непрерывным воспроизведением.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- сообщение MCIWNDM_SETREPEAT Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158e0b52f01431886fd8a70e89efadfdd7335258c0808cdb6780bf06071e3280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807594"
---
# <a name="mciwndm_setrepeat-message"></a>\_Сообщение мЦивндм сетрепеат

Сообщение **мЦивндм \_ сетрепеат** устанавливает флаг повтора, связанный с непрерывным воспроизведением. Сообщение **мЦивндм \_ сетрепеат** работает совместно с командой [MCI \_ Play](mci-play.md) , чтобы обеспечить непрерывный цикл воспроизведения. Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетрепеат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="f"></span><span id="F"></span>*ж*
</dt> <dd>

Новое состояние флага повтора. Укажите **значение true** , чтобы включить непрерывное воспроизведение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль.

## <a name="remarks"></a>Remarks

В настоящее время МЦИАВИ является единственным устройством, поддерживающим непрерывное воспроизведение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[\_Воспроизведение MCI](mci-play.md)
</dt> <dt>

[**мЦивндсетрепеат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





