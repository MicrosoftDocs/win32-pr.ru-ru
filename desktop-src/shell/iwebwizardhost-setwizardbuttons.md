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
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985785"
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

## <a name="remarks"></a>Примечания

Не забудьте реализовать функции обработчика на каждой странице на стороне сервера для функций onback () и onback (), соответствующих кнопкам мастера **назад** и **Далее**. Функции onback () и onback () отвечают на **сетвизардбуттонс**. В соответствующее время функция OnNext () вызывает **сетвизардбуттонс** с *вбластпаже* = **true**, что может включить кнопку **Готово** . OnNext () также вызывает [**финалнекст**](iwebwizardhost-finalnext.md) , когда пользователь нажимает кнопку **Готово** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl> |



 

 




