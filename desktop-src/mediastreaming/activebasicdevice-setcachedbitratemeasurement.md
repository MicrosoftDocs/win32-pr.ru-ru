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
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492867"
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

 

