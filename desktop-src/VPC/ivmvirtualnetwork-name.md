---
title: Свойство имени Ивмвиртуалнетворк (Впккоминтерфацес. h)
description: Уникальное имя экземпляра виртуальной сети.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Имя свойство Virtual PC
- Имя свойство Virtual PC, интерфейс Ивмвиртуалнетворк
- Ивмвиртуалнетворк интерфейс Virtual PC, свойство Name
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79cd7ba9e06c7e3ed8c2788d749d5a010b1299bfd4c635570ff161197e70c22f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122653"
---
# <a name="ivmvirtualnetworkname-property"></a>Свойство Ивмвиртуалнетворк:: Name

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает уникальное имя экземпляра виртуальной сети.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a>Значение свойства

Имя виртуальной сети.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>                                                |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>                                                   |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка, или экземпляр виртуальной сети неизвестен.<br/> |



## <a name="remarks"></a>Remarks

Имена виртуальных сетей не учитывают регистр, например "Минетворк" и "минетворк" ссылаются на одну и ту же виртуальную сеть.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалнетворк определен как 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмвиртуалнетворк**](ivmvirtualnetwork.md)
</dt> </dl>

 

