---
title: Итссбклиентконнектион, свойство домена
description: Извлекает значение, указывающее доменное имя клиента подключение к удаленному рабочему столу (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойств домена
- Службы удаленных рабочих столов свойств домена, интерфейс Итссбклиентконнектион
- Службы удаленных рабочих столов интерфейса Итссбклиентконнектион, свойство Domain
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc99724eb419e831e65f402299aa1603be07ab2ab5a88e0ba9b056492514865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511514"
---
# <a name="itssbclientconnectiondomain-property"></a>Итссбклиентконнектион: свойство омаин:D

Извлекает значение, указывающее доменное имя клиента подключение к удаленному рабочему столу (RDC).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Значение свойства

Указатель на переменную **BSTR** , содержащую доменное имя клиента RDC. После завершения использования строки освободите ее, вызвав функцию [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Сбтсв. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**итссбклиентконнектион**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

