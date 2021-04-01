---
title: Имсрдпдевице Девицеинстанцеид, свойство
description: Возвращает идентификатор экземпляра устройства.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицеинстанцеид
- Службы удаленных рабочих столов свойства Девицеинстанцеид, интерфейс Имсрдпдевице
- Службы удаленных рабочих столов интерфейса Имсрдпдевице, свойство Девицеинстанцеид
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a159911e4294e2207ad4ae989d4ef9e390384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989410"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a>Имсрдпдевице: свойство Евицеинстанцеид:D

Возвращает идентификатор экземпляра устройства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a>Значение свойства

Идентификатор экземпляра устройства.

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпдевице определен как 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпдевице**](imsrdpdevice.md)
</dt> </dl>

 

 





