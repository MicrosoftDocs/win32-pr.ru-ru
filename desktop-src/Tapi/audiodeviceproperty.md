---
description: 'Перечисление Аудиодевицепроперти используется методами Итаудиодевицеконтрол::, Итаудиодевицеконтрол:: Get и Итаудиодевицеконтрол:: Set для указания свойства, для которого выполняется обращение.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Перечисление Аудиодевицепроперти (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675637"
---
# <a name="audiodeviceproperty-enumeration"></a>Перечисление Аудиодевицепроперти

\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Перечисление **аудиодевицепроперти** используется методами [**итаудиодевицеконтрол::**](itaudiodevicecontrol-getrange.md), [**Итаудиодевицеконтрол:: Get**](itaudiodevicecontrol-get.md)и [**итаудиодевицеконтрол:: Set**](itaudiodevicecontrol-set.md) для указания свойства, для которого выполняется обращение.

## <a name="syntax"></a>Синтаксис


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**Аудиодевице \_ дуплексмоде**
</dt> <dd>

Указывает, что режим дуплекса устройства устанавливается или извлекается.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**Аудиодевице \_ аутоматикгаинконтрол**
</dt> <dd>

Указывает, что устанавливается или извлекается автоматический контроль усиления устройства.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**Аудиодевице \_ акаустицечоканцеллатион**
</dt> <dd>

Указывает, что задаются или извлекаются свойства отмены акустического эха устройства.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ипмсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Итаудиодевицеконтрол:: Range**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**Итаудиодевицеконтрол:: Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**Итаудиодевицеконтрол:: Set**](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




