---
description: Метод Set задает значение заданного свойства качества потока.
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'Метод Итстреамкуалитиконтрол:: Set (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675609"
---
# <a name="itstreamqualitycontrolset-method"></a>Метод Итстреамкуалитиконтрол:: Set

\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **Set** задает значение заданного [**свойства качества потока**](streamqualityproperty.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Свойство* \[ окне\]
</dt> <dd>

Член перечисления [**стреамкуалитипроперти**](streamqualityproperty.md) .

</dd> <dt>

*lvalue* \[ окне\]
</dt> <dd>

Требуемое значение для входного *Свойства*.

</dd> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как должно контролироваться значение *свойства* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Значение                                                                                         | Значение                                                         |
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

[**итстреамкуалитиконтрол**](itstreamqualitycontrol.md)
</dt> <dt>

[**тапиконтролфлагс**](tapicontrolflags.md)
</dt> <dt>

[**стреамкуалитипроперти**](streamqualityproperty.md)
</dt> </dl>

 

 




