---
title: Рпктрексцепт (RPC. h)
description: Инструкция Рпктрексцепт обеспечивает структурированную обработку исключений для приложений RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- Рпктрексцепт RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c7a73ca80eb342b9a23fcaa4b922afe8d19f00e1f22ab82f8c6027ecc43d76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925971"
---
# <a name="rpctryexcept"></a>рпктрексцепт

Инструкция **рпктрексцепт** обеспечивает структурированную обработку исключений для приложений RPC. Если любая из инструкций программы в **рпктрексцепт** вызывает исключение, выполняются инструкции в блоке кода [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) . Все инструкции **рпктрексцепт** должны завершаться инструкцией [**рпцендексцепт**](/previous-versions/aa375629(v=vs.80)) .

Дополнительные сведения см. в разделе [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

**Windows Vista и более поздних версий Windows:**[**рпцексцептионфилтер**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) рекомендуется для структурированной обработки исключений наиболее распространенных исключений в качестве альтернативы настраиваемым фильтрам с помощью [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).  

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**рпцексцептионфилтер**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**рпктрифиналли**](rpctryfinally.md)
</dt> </dl>

 

