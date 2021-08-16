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
ms.openlocfilehash: 36b40d0831c18a7931f3f29492dd4c7769440a76ddcec2aa33ba3e840e97950d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859127"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl> |



 

 




