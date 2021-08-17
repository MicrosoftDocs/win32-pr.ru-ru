---
title: Метод WSMan. Креатеконнектионоптионс (Всмандисп. h)
description: Создает объект ConnectionOptions, который указывает имя пользователя и пароль, используемые при создании сеанса.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода креатеконнектионоптионс
- служба удаленного управления Windows метода креатеконнектионоптионс, объект WSMan
- объект WSMan служба удаленного управления Windows, метод креатеконнектионоптионс
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4bd1218fcf6ca228cbc7538434b00b7b4e80d4c5b2df54807e031c11c14f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742671"
---
# <a name="wsmancreateconnectionoptions-method"></a>Метод WSMan. Креатеконнектионоптионс

Создает объект [**ConnectionOptions**](connectionoptions.md) , который указывает имя пользователя и пароль, используемые при создании сеанса.

## <a name="syntax"></a>Синтаксис


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Объект [**ConnectionOptions**](connectionoptions.md) , который используется для указания пары имя пользователя и пароль, которые используются для идентификации пользователя при проверке подлинности.

## <a name="remarks"></a>Remarks

Для вызова этого метода используется следующий синтаксис.


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





