---
title: Метод Активебасикдевице Сеткачедбитратемеасуремент (Плайтодевице. h)
description: Задает кэшированную скорость.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- API потоковой передачи мультимедиа метода Сеткачедбитратемеасуремент
- API потоковой передачи мультимедиа метода Сеткачедбитратемеасуремент, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Сеткачедбитратемеасуремент
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf79b7e9066aacfcce1f82c998463d6d620f5061fef4af788104a0c01a44ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952774"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>Метод Активебасикдевице:: Сеткачедбитратемеасуремент

Задает кэшированную скорость.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetCachedBitrateMeasurement(
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

Значение, для которого устанавливается скорость.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Плайтодевице. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Плайтодевице. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

