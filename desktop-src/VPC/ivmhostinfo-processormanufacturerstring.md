---
title: Свойство Процессормануфактурерстринг Ивмхостинфо (Впккоминтерфацес. h)
description: Получает изготовителя хоста процессора.
ms.assetid: b7f4a03a-184c-4996-8102-994bf7f37e50
keywords:
- Процессормануфактурерстринг свойство Virtual PC
- Процессормануфактурерстринг свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Процессормануфактурерстринг
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorManufacturerString
- IVMHostInfo.get_ProcessorManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029e64f0a13d84bea118498726893620e058ac83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071068"
---
# <a name="ivmhostinfoprocessormanufacturerstring-property"></a>Ивмхостинфо: свойство Роцессормануфактурерстринг:P

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает изготовителя хоста процессора.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ProcessorManufacturerString(
  [out, retval] BSTR *processorManufacturerString
);
```



## <a name="property-value"></a>Значение свойства

Производитель.

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

 

