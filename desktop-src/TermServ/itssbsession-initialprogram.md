---
title: Итссбсессион Инитиалпрограм, свойство
description: Возвращает или задает начальную программу для данного сеанса.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Инитиалпрограм
- Службы удаленных рабочих столов свойства Инитиалпрограм, интерфейс Итссбсессион
- Службы удаленных рабочих столов интерфейса Итссбсессион, свойство Инитиалпрограм
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490620"
---
# <a name="itssbsessioninitialprogram-property"></a>Свойство Итссбсессион:: Инитиалпрограм

Возвращает или задает начальную программу для данного сеанса. Начальная программа — это программа, которая запускается при запуске сеанса пользователя.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a>Значение свойства

Переменная **BSTR** , содержащая начальную программу.

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

 

 





