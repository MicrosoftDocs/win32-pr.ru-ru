---
title: Свойство Продукттипе Ивмгуестос (Впккоминтерфацес. h)
description: Возвращает тип продукта гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Продукттипе свойство Virtual PC
- Продукттипе свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Продукттипе
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672651"
---
# <a name="ivmguestosproducttype-property"></a>Ивмгуестос: свойство Родукттипе:P

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает тип продукта гостевой операционной системы, работающей на виртуальной машине.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a>Значение свойства

Тип продукта. Поддерживаются следующие строковые значения.



| Значение                                                                                  | Значение                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x0000002"</dt> </dl> | Система является контроллером домена, а операционной системой является Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 или Windows 2000 Server.<br/>                                                                                                   |
| <dl> <dt>"0x0000003"</dt> </dl> | Операционная система — Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 или Windows 2000 Server.<br/> Обратите внимание, что сервер, который также является контроллером домена, сообщается как **\_ \_ \_ контроллер домена ver NT**, а не **\_ \_ сервер ver NT**.<br/> |
| <dl> <dt>"0x0000001"</dt> </dl> | Операционная система — Windows 7, Windows Vista, Windows XP или Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмгуестос**](ivmguestos.md)
</dt> </dl>

 

