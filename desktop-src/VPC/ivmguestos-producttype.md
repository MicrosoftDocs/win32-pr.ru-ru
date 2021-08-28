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
ms.openlocfilehash: 0c31b3b91cf75687d82e02e3b97c78dd0e40f724756b609a3e2b60c73812ee5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512314"
---
# <a name="ivmguestosproducttype-property"></a>Ивмгуестос: свойство Родукттипе:P

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>"0x0000002"</dt> </dl> | система является контроллером домена, а операционная система — Windows server 2008 r2, Windows server 2008, Windows server 2003 r2, Windows server 2003 или Windows 2000 server.<br/>                                                                                                   |
| <dl> <dt>"0x0000003"</dt> </dl> | операционная система — Windows server 2008 r2, Windows server 2008, Windows server 2003 R2, Windows server 2003 или Windows 2000 server.<br/> Обратите внимание, что сервер, который также является контроллером домена, сообщается как **\_ \_ \_ контроллер домена ver NT**, а не **\_ \_ сервер ver NT**.<br/> |
| <dl> <dt>"0x0000001"</dt> </dl> | операционная система — Windows 7, Windows Vista, Windows XP или Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмгуестос**](ivmguestos.md)
</dt> </dl>

 

