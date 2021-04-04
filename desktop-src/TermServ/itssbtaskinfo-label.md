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
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803779"
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

 

 





