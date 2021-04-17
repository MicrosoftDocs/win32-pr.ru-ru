---
description: Метод Set задает значение заданного свойства звукового устройства.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'Метод Итаудиодевицеконтрол:: Set (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675060"
---
# <a name="itaudiodevicecontrolset-method"></a>Метод Итаудиодевицеконтрол:: Set

\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **Set** задает значение заданного [**Свойства звукового устройства**](audiodeviceproperty.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Свойство* \[ окне\]
</dt> <dd>

Член перечисления [**аудиодевицепроперти**](audiodeviceproperty.md) .

</dd> <dt>

*lvalue* \[ окне\]
</dt> <dd>

Требуемое значение для свойства.

</dd> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как должно контролироваться значение *свойства* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                                   | Описание                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Метод успешно выполнен.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для выполнения операции.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|--------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ипмсп. h</dt> </dl>   |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итаудиодевицеконтрол**](itaudiodevicecontrol.md)
</dt> <dt>

[**тапиконтролфлагс**](tapicontrolflags.md)
</dt> <dt>

[**аудиодевицепроперти**](audiodeviceproperty.md)
</dt> </dl>

 

 




