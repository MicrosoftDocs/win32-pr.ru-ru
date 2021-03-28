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
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910459"
---
# <a name="webwizardhostfinalback-method"></a>Вебвизардхост. Финалбакк, метод

Переход к странице на стороне клиента, непосредственно предшествующей странице, на которой размещены HTML-страницы на стороне сервера.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="remarks"></a>Примечания

Когда мастер отображает первую страницу на стороне сервера и пользователь нажимает кнопку « **назад** », сервер вызывает **финалбакк** при уведомлении этого события обработчиком событий клиента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl> |



 

 




