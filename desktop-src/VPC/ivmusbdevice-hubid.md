---
title: Свойство Хубид Ивмусбдевице (Впккоминтерфацес. h)
description: Возвращает идентификатор концентратора, к которому подключено устройство.
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- Хубид свойство Virtual PC
- Хубид свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Хубид
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d36047722206c2dfd52f4fc14c8e98270db4cab2d62f0694ea3f44bac10449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958713"
---
# <a name="ivmusbdevicehubid-property"></a>Свойство Ивмусбдевице:: Хубид

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает идентификатор концентратора, к которому подключено устройство.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a>Значение свойства

Идентификатор концентратора. Это значение назначается драйвером соединителя USB.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                            | Значение                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>               | Метод завершился успешно.<br/> |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl> | Параметр имеет **значение NULL**.<br/>         |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмусбдевице**](ivmusbdevice.md)
</dt> </dl>

 

