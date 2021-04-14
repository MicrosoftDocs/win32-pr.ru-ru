---
title: Свойство UserName Итссбклиентконнектион
description: Извлекает значение, указывающее имя пользователя, инициировавшего подключение.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства имени пользователя
- Свойство UserName службы удаленных рабочих столов, интерфейс Итссбклиентконнектион
- Службы удаленных рабочих столов интерфейса Итссбклиентконнектион, свойство UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341145"
---
# <a name="itssbclientconnectionusername-property"></a>Свойство Итссбклиентконнектион:: UserName

Извлекает значение, указывающее имя пользователя, инициировавшего подключение.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Значение свойства

Указатель на имя пользователя. После завершения использования строки освободите ее, вызвав функцию [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Сбтсв. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итссбклиентконнектион**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

