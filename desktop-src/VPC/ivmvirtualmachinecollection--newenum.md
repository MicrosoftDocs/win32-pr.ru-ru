---
title: Свойство _NewEnum Ивмвиртуалмачинеколлектион (Впккоминтерфацес. h)
description: Возвращает перечислитель для коллекции. | Свойство _NewEnum Ивмвиртуалмачинеколлектион (Впккоминтерфацес. h)
ms.assetid: 86b51542-139c-4e2b-baec-2c90956d99b3
keywords:
- _NewEnum свойств Virtual PC
- _NewEnum свойств Virtual PC, интерфейс Ивмвиртуалмачинеколлектион
- Ивмвиртуалмачинеколлектион интерфейс Virtual PC, свойство _NewEnum
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection._NewEnum
- IVMVirtualMachineCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea610b005ea9482d59de65311256f77446e442cd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353212"
---
# <a name="ivmvirtualmachinecollection_newenum-property"></a>Свойство Ивмвиртуалмачинеколлектион:: \_ NewEnum

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает перечислитель для коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Значение свойства

Перечислитель [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/> |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>    |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                           |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>  |
| IID<br/>                      | IID \_ ивмвиртуалмачинеколлектион определен как 59f31786-2a3d-4fbf-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачинеколлектион**](ivmvirtualmachinecollection.md)
</dt> </dl>

 

