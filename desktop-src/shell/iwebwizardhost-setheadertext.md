---
description: Задает заголовок и подзаголовок, которые отображаются в заголовке мастера. В общем случае клиент отобразит заголовок над HTML и под заголовком окна.
title: Вебвизардхост. Сесеадертекст, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841835"
---
# <a name="webwizardhostsetheadertext-method"></a>Вебвизардхост. Сесеадертекст, метод

Задает заголовок и подзаголовок, которые отображаются в заголовке мастера. В общем случае клиент отобразит заголовок над HTML и под заголовком окна.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрхеадертитле* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Строка, содержащая заголовок.

</dd> <dt>

*бстрхеадерсубтитле* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Строка, содержащая подзаголовок.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl> |



 

 
