---
title: Свойство Меморяваилстринг Ивмхостинфо (Впккоминтерфацес. h)
description: Извлекает объем доступной физической памяти на хост-компьютере в мегабайтах в виде строки.
ms.assetid: a0f17dda-2042-4aec-9968-6662d32684cf
keywords:
- Меморяваилстринг свойство Virtual PC
- Меморяваилстринг свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Меморяваилстринг
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvailString
- IVMHostInfo.get_MemoryAvailString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea003b94d0d4604dfba3daf545a51b9d69b6708c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491307"
---
# <a name="ivmhostinfomemoryavailstring-property"></a>Свойство Ивмхостинфо:: Меморяваилстринг

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает объем доступной физической памяти на хост-компьютере в мегабайтах в виде строки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_MemoryAvailString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a>Значение свойства

Доступный объем физической памяти в мегабайтах.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмхостинфо**](ivmhostinfo.md)
</dt> </dl>

 

