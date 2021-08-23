---
description: Метод Set задает значение заданного свойства контроля качества вызова.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'Метод Иткаллкуалитиконтрол:: Set (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5506e4c318440c2b611a2404590bdf638d34a7da2353a5598d09aecf2990668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003392"
---
# <a name="itcallqualitycontrolset-method"></a>Метод Иткаллкуалитиконтрол:: Set

\[этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **Set** задает значение заданного [Свойства контроля качества вызова](callqualityproperty.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Свойство* \[ окне\]
</dt> <dd>

Член перечисления [**каллкуалитипроперти**](callqualityproperty.md) .

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

 

 




