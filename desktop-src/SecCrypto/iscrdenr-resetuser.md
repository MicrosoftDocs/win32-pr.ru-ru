---
description: Удаляет имя пользователя из элемента управления смарт-картой.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'Метод Искрденр:: Ресетусер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664396"
---
# <a name="iscrdenrresetuser-method"></a>Метод Искрденр:: Ресетусер

Метод **ресетусер** удаляет имя пользователя из элемента управления смарт-картой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT resetUser();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="remarks"></a>Комментарии

Этот метод очищает все существующие имя пользователя и ранее зарегистрированный сертификат из памяти. Однако ранее зарегистрированный сертификат не удаляется со смарт-карты.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искрденр**](iscrdenr.md)
</dt> <dt>

[**Искрденр:: имя пользователя**](iscrdenr-getusername.md)
</dt> <dt>

[**Искрденр:: Селектусернаме**](iscrdenr-selectusername.md)
</dt> <dt>

[**Искрденр:: Сетусернаме**](iscrdenr-setusername.md)
</dt> </dl>

 

 




