---
title: Свойство Ивмхостинфо MMX (Впккоминтерфацес. h)
description: Определяет, поддерживает ли процессор набор инструкций MMX. | Свойство Ивмхостинфо MMX (Впккоминтерфацес. h)
ms.assetid: 2f556289-c752-4af2-a6d0-abb6e717e609
keywords:
- Виртуальное устройство MMX свойство Virtual PC
- Свойство MMX Virtual PC, интерфейс Ивмхостинфо
- Интерфейс Ивмхостинфо Virtual PC, свойство MMX
topic_type:
- apiref
api_name:
- IVMHostInfo.MMX
- IVMHostInfo.get_MMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4498289130a59e7c651b9dfffe9d4d228f9d9187e9d958ce1d203291654d7c53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998904"
---
# <a name="ivmhostinfommx-property"></a>Свойство Ивмхостинфо:: MMX

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет, поддерживает ли процессор набор инструкций MMX.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_MMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a>Значение свойства

**Значение true** , если инструкции MMX поддерживаются; в противном случае — **значение false** .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмхостинфо**](ivmhostinfo.md)
</dt> </dl>

 

