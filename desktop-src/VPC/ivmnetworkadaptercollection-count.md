---
title: Свойство Ивмнетворкадаптерколлектион Count (Впккоминтерфацес. h)
description: Возвращает число сетевых интерфейсов в этой коллекции.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмнетворкадаптерколлектион
- Ивмнетворкадаптерколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c2d9e2a76df3d73668983c37bd087a2c2cbd536b10a880955abae6ed8dd14f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866844"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a>Свойство Ивмнетворкадаптерколлектион:: count

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает число сетевых интерфейсов в этой коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Значение свойства

Число сетевых интерфейсов.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                           |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                  |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>  |
| IID<br/>                      | IID \_ ивмнетворкадаптерколлектион определен как ebaeafe9-EBCD-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмнетворкадаптерколлектион**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

