---
title: Ивмдрмдевице Исвмдрмдевице, метод
description: метод исвмдрмдевице определяет, поддерживает ли устройство Windows Media DRM 10 для переносных устройств.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Метод Исвмдрмдевице Windows Media диспетчер устройств
- Метод Исвмдрмдевице Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Исвмдрмдевице
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ee225267ce2301e9a2dad392d72ce72b0e698872cd3fd54ab3e50a07043477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957264"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>Метод Ивмдрмдевице:: Исвмдрмдевице

метод **исвмдрмдевице** определяет, поддерживает ли устройство Windows Media DRM 10 для переносных устройств.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдвверсион* \[ заполняет\]
</dt> <dd>

версия Windows Media DRM 10 для переносных устройств со значением 0x00010000.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ВМДДРМСП. idl</dt> </dl> |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмдевице**](iwmdrmdevice.md)
</dt> </dl>

 

 





