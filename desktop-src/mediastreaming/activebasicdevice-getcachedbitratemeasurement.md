---
title: Метод Активебасикдевице Жеткачедбитратемеасуремент (Плайтодевице. h)
description: Возвращает кэшированную скорость.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API потоковой передачи мультимедиа метода Жеткачедбитратемеасуремент
- API потоковой передачи мультимедиа метода Жеткачедбитратемеасуремент, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Жеткачедбитратемеасуремент
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 031d77595298651be11c793f8fd96471808ab1aef3f5a2b6398be9c1ff10de02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236869"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a>Метод Активебасикдевице:: Жеткачедбитратемеасуремент

Возвращает кэшированную скорость.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фисикалнетворкинтерфаце* \[ окне\]
</dt> <dd>

Указывает физический сетевой интерфейс.

</dd> <dt>

*скорость* \[ out, retval\]
</dt> <dd>

Получает значение скорости.

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

 

