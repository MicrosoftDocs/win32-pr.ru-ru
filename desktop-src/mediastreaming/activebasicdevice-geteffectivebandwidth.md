---
title: Метод Активебасикдевице Жетеффективебандвидс (Плайтодевице. h)
description: Возвращает текущую эффективную пропускную способность для устройства.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API потоковой передачи мультимедиа метода Жетеффективебандвидс
- API потоковой передачи мультимедиа метода Жетеффективебандвидс, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Жетеффективебандвидс
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071975"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>Метод Активебасикдевице:: Жетеффективебандвидс

Возвращает текущую эффективную пропускную способность для устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*трансмитспид* \[ в, retval\]
</dt> <dd>

Указывает, получается ли скорость передачи или получается скорость приема.

**значение true** , чтобы получить скорость передачи. **значение false** , чтобы получить скорость приема.

</dd> <dt>

*куррентспид* \[ заполняет\]
</dt> <dd>

Получает текущую эффективную пропускную способность.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Плайтодевице. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Плайтодевице. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

