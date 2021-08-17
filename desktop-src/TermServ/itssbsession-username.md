---
title: Свойство UserName Итссбсессион
description: Возвращает имя пользователя для этого сеанса.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства имени пользователя
- Свойство UserName службы удаленных рабочих столов, интерфейс Итссбсессион
- Службы удаленных рабочих столов интерфейса Итссбсессион, свойство UserName
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d42c06d700cb95df5635f902876c242b164a6fd12415848cc11539cb30edd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351204"
---
# <a name="itssbsessionusername-property"></a>Свойство Итссбсессион:: username

Возвращает имя пользователя для этого сеанса.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a>Значение свойства

Указатель на переменную **BSTR** , которая получает имя пользователя для этого сеанса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Сбтсв. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итссбсессион**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





