---
title: Сообщение MCIWNDM_SETREPEAT (VFW. h)
description: Сообщение МЦИВНДМ \_ сетрепеат устанавливает флаг повтора, связанный с непрерывным воспроизведением.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT сообщения Windows мультимедиа
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
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892265"
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

## <a name="remarks"></a>Комментарии

В настоящее время МЦИАВИ является единственным устройством, поддерживающим непрерывное воспроизведение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[\_Воспроизведение MCI](mci-play.md)
</dt> <dt>

[**мЦивндсетрепеат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





