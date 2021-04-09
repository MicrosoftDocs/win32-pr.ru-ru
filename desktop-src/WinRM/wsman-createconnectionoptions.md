---
title: Метод WSMan. Креатеконнектионоптионс (Всмандисп. h)
description: Создает объект ConnectionOptions, который указывает имя пользователя и пароль, используемые при создании сеанса.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Креатеконнектионоптионс
- Служба удаленного управления Windows метода Креатеконнектионоптионс, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Креатеконнектионоптионс
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
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891665"
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

## <a name="remarks"></a>Комментарии

Для вызова этого метода используется следующий синтаксис.


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





