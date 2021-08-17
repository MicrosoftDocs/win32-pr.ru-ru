---
title: Итссбсессион, свойство TargetName
description: Возвращает имя целевого объекта, на котором был создан этот сеанс.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Свойство TargetName службы удаленных рабочих столов
- Свойство TargetName службы удаленных рабочих столов, интерфейс Итссбсессион
- Службы удаленных рабочих столов интерфейса Итссбсессион, свойство TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbc1e26aa4bf55a59b6405921d49e6b1aafa14e63a1e487caca9a7c036b1524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138317"
---
# <a name="itssbsessiontargetname-property"></a>Свойство Итссбсессион:: TargetName

Возвращает имя целевого объекта, на котором был создан этот сеанс.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a>Значение свойства

Указатель на переменную **BSTR** , которая получает имя целевого объекта, на котором был создан этот сеанс.

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

 

 





