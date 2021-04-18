---
title: Метод Активебасикдевице Сеткачедсинкпротоколинфо (Плайтодевице. h)
description: Возвращает сведения о кэшированном протоколе приемника для устройства. | Метод Активебасикдевице Сеткачедсинкпротоколинфо (Плайтодевице. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- API потоковой передачи мультимедиа метода Сеткачедсинкпротоколинфо
- API потоковой передачи мультимедиа метода Сеткачедсинкпротоколинфо, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Сеткачедсинкпротоколинфо
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703613"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a>Метод Активебасикдевице:: Сеткачедсинкпротоколинфо

Возвращает сведения о кэшированном протоколе приемника для устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фисикалнетворкинтерфаце* \[ окне\]
</dt> <dd>

Указывает физический сетевой интерфейс.

</dd> <dt>

*скорость* \[ окне\]
</dt> <dd>

Значение скорости.

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

 

