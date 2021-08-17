---
title: Итссбтаскинфо, свойство метки
description: Извлекает метку, которая описывает назначение задачи.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства метки
- Свойство метки службы удаленных рабочих столов, интерфейс Итссбтаскинфо
- Службы удаленных рабочих столов интерфейса Итссбтаскинфо, свойство Label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2414dd83d44add4084a4176f575817875e933f9770039e49b02364bd8103cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138307"
---
# <a name="itssbtaskinfolabel-property"></a>Итссбтаскинфо:: Label, свойство

Извлекает метку, которая описывает назначение задачи.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a>Значение свойства

Указатель на значение **BSTR** , содержащее метку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Сбтсв. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итссбтаскинфо**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





