---
title: Свойство Ивмвиртуалнетворкколлектион Count (Впккоминтерфацес. h)
description: Извлекает число виртуальных сетей в этой коллекции.
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмвиртуалнетворкколлектион
- Ивмвиртуалнетворкколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe472ee2e81495284377bab4a59a55bdf07ccf43f636769abcab391fe97ad60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592332"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a>Свойство Ивмвиртуалнетворкколлектион:: count

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает число виртуальных сетей в этой коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Значение свойства

Число виртуальных сетей.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                           |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                  |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>  |
| IID<br/>                      | IID \_ ивмвиртуалнетворкколлектион определен как 8ed680be-4242-4b2a-a21c-1982d8b0f675<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалнетворкколлектион**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

