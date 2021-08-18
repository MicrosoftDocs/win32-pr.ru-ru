---
description: Метод Get получает значение заданного свойства контроля качества вызова.
ms.assetid: 0fec408e-2751-4c99-afe1-4337d22eff83
title: 'Метод Иткаллкуалитиконтрол:: Get (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ed08a7b8f166e267b32a80416387bd309c0c3a60e4ee06117ae9b8c43e037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003412"
---
# <a name="itcallqualitycontrolget-method"></a>Метод Иткаллкуалитиконтрол:: Get

\[этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **Get** получает значение заданного [Свойства контроля качества вызова](callqualityproperty.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Get(
  [in]  CallQualityProperty Property,
  [out] long                *plValue,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Свойство* \[ окне\]
</dt> <dd>

Член перечисления [**каллкуалитипроперти**](callqualityproperty.md) .

</dd> <dt>

*плвалуе* \[ заполняет\]
</dt> <dd>

Значение входного *Свойства*.

</dd> <dt>

*плфлагс* \[ заполняет\]
</dt> <dd>

Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как управляется значение *свойства* .

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
| Заголовок<br/>       | <dl> <dt>Ипмсп. h</dt> </dl>   |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иткаллкуалитиконтрол**](itcallqualitycontrol.md)
</dt> <dt>

[**тапиконтролфлагс**](tapicontrolflags.md)
</dt> <dt>

[**каллкуалитипроперти**](callqualityproperty.md)
</dt> </dl>

 

 




