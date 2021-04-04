---
title: Итссбтаскинфо, свойство состояния
description: Извлекает \_ \_ значение перечисления состояния задачи RDV, представляющее состояние задачи.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Свойство Status службы удаленных рабочих столов
- Свойство Status службы удаленных рабочих столов, интерфейс Итссбтаскинфо
- Службы удаленных рабочих столов интерфейса Итссбтаскинфо, свойство Status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802134"
---
# <a name="itssbtaskinfostatus-property"></a>Свойство Итссбтаскинфо:: Status

Извлекает значение [**перечисления \_ \_ состояния задачи RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , представляющее состояние задачи.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a>Значение свойства

Значение [**перечисления \_ \_ состояния задачи RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , представляющее состояние задачи.

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

 

 





