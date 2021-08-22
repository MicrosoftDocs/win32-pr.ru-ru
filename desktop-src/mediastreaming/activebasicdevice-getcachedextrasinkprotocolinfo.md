---
title: Метод Активебасикдевице Жеткачедекстрасинкпротоколинфо (Плайтодевице. h)
description: Возвращает дополнительные кэшированные сведения о протоколе приемника для устройства.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- API потоковой передачи мультимедиа метода Жеткачедекстрасинкпротоколинфо
- API потоковой передачи мультимедиа метода Жеткачедекстрасинкпротоколинфо, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Жеткачедекстрасинкпротоколинфо
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf4508c40fd0abcb0df809216a9bae1d8811c8a8bd79bfb31dfbbd5062ddce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736410"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a>Метод Активебасикдевице:: Жеткачедекстрасинкпротоколинфо

Возвращает дополнительные кэшированные сведения о протоколе приемника для устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Дополнительные кэшированные сведения о протоколе приемника для устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Плайтодевице. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Плайтодевице. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

