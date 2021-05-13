---
description: Обновляет кнопки назад, далее и готово в кадре мастера клиента.
title: Вебвизардхост. Сетвизардбуттонс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842625"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Вебвизардхост. Сетвизардбуттонс, метод

Обновляет кнопки **назад**, **Далее** и **Готово** в кадре мастера клиента.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вбенаблебакк* \[ окне\]
</dt> <dd>

Тип: **Boolean**

Включает кнопку " **назад** ".

</dd> <dt>

*вбенабленекст* \[ окне\]
</dt> <dd>

Тип: **Boolean**

Становится активной кнопка **Далее**.

</dd> <dt>

*вбластпаже* \[ окне\]
</dt> <dd>

Тип: **Boolean**

Включает кнопку **Готово** . Указывает, что это последняя страница на стороне сервера.

</dd> </dl>

## <a name="remarks"></a>Remarks

Не забудьте реализовать функции обработчика на каждой странице на стороне сервера для функций onback () и onback (), соответствующих кнопкам мастера **назад** и **Далее**. Функции onback () и onback () отвечают на **сетвизардбуттонс**. В соответствующее время функция OnNext () вызывает **сетвизардбуттонс** с *вбластпаже* = **true**, что может включить кнопку **Готово** . OnNext () также вызывает [**финалнекст**](iwebwizardhost-finalnext.md) , когда пользователь нажимает кнопку **Готово** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl> |



 

 




