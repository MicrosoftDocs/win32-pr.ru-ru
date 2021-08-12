---
title: Свойство Дривенумбер Ивмфлоппидриве (Впккоминтерфацес. h)
description: Возвращает отсчитываемый от нуля индекс контроллера, к которому подключен флоппи-дисковод.
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- Дривенумбер свойство Virtual PC
- Дривенумбер свойство Virtual PC, интерфейс Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, свойство Дривенумбер
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5a72b9546949a4cd8b2450a3ed41e90d598dc306974a13c7b0dfcf2fe5c232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595363"
---
# <a name="ivmfloppydrivedrivenumber-property"></a>Ивмфлоппидриве: свойство Ривенумбер:D

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает отсчитываемый от нуля индекс контроллера, к которому подключен флоппи-дисковод.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a>Значение свойства

Отсчитываемый от нуля индекс контроллера.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмфлоппидриве**](ivmfloppydrive.md)
</dt> </dl>

 

