---
description: Переход к странице на стороне клиента, непосредственно предшествующей странице, на которой размещены HTML-страницы на стороне сервера.
title: Вебвизардхост. Финалбакк, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841875"
---
# <a name="webwizardhostfinalback-method"></a>Вебвизардхост. Финалбакк, метод

Переход к странице на стороне клиента, непосредственно предшествующей странице, на которой размещены HTML-страницы на стороне сервера.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="remarks"></a>Remarks

Когда мастер отображает первую страницу на стороне сервера и пользователь нажимает кнопку « **назад** », сервер вызывает **финалбакк** при уведомлении этого события обработчиком событий клиента.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl> |



 

 




