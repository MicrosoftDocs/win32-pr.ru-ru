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
ms.openlocfilehash: 7ac51318997e80c043e36dc87b052a5e21bf9933f93e34f2e5071fb20d4bb75b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236786"
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
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Плайтодевице. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Плайтодевице. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

