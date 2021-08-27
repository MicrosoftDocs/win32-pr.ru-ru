---
description: Метод Get получает значение заданного свойства качества потока.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: 'Метод Итстреамкуалитиконтрол:: Get (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1a82a448320115664ab0664c2f7d8cde9f8049c7ee2cb86ccf7e46f856ceafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080504"
---
# <a name="itstreamqualitycontrolget-method"></a>Метод Итстреамкуалитиконтрол:: Get

\[этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **Get** получает значение заданного [**свойства качества потока**](streamqualityproperty.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Свойство* \[ окне\]
</dt> <dd>

Член перечисления [**стреамкуалитипроперти**](streamqualityproperty.md) .

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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|--------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,1<br/>                                                         |
| Заголовок<br/>       | <dl> <dt>Ипмсп. h</dt> </dl>   |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**итстреамкуалитиконтрол**](itstreamqualitycontrol.md)
</dt> <dt>

[**тапиконтролфлагс**](tapicontrolflags.md)
</dt> <dt>

[**стреамкуалитипроперти**](streamqualityproperty.md)
</dt> </dl>

 

 




