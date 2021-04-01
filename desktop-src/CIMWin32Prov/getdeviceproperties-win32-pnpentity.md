---
description: Возвращает указанные свойства данного устройства самонастраивающийся.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Метод Жетдевицепропертиес класса Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072413"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a>Метод Жетдевицепропертиес \_ класса Win32 пнпентити

Возвращает указанные свойства данного устройства самонастраивающийся.

## <a name="syntax"></a>Синтаксис


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*девицепропертикэйс* \[ в необязательное\]
</dt> <dd>

Возвращаемые свойства.

</dd> <dt>

*девицепропертиес* \[ заполняет\]
</dt> <dd>

Запрошенные свойства в соответствующих подтипах абстрактного класса [**Win32 \_ пнпдевицепроперти**](win32-pnpdeviceproperty.md) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Пнпентити Win32**](win32-pnpentity.md)
</dt> </dl>

 

 




