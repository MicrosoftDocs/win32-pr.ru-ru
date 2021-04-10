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
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136363"
---
# <a name="rpctryexcept"></a>рпктрексцепт

Инструкция **рпктрексцепт** обеспечивает структурированную обработку исключений для приложений RPC. Если любая из инструкций программы в **рпктрексцепт** вызывает исключение, выполняются инструкции в блоке кода [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) . Все инструкции **рпктрексцепт** должны завершаться инструкцией [**рпцендексцепт**](/previous-versions/aa375629(v=vs.80)) .

Дополнительные сведения см. в разделе [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

**Windows Vista и более поздние версии Windows:**  [**рпцексцептионфилтер**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) рекомендуется для структурированной обработки исключений наиболее распространенных исключений в качестве альтернативы настраиваемым фильтрам с помощью [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

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

 

