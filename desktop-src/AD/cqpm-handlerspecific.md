---
title: Сообщение CQPM_HANDLERSPECIFIC (Кмнкуери. h)
description: Базовое значение, используемое для сообщений, являющихся частными для обработчика запросов.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_HANDLERSPECIFIC Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489477"
---
# <a name="cqpm_handlerspecific-message"></a>\_Сообщение ККПМ хандлерспеЦифик

Сообщение **ККПМ \_ хандлерспеЦифик** — это базовое значение, используемое для сообщений, которые являются частными для обработчика запросов. Обработчик запросов должен добавить это значение в частные сообщения, чтобы избежать конфликтов сообщений.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Содержит дополнительные данные сообщения. Содержимое этого параметра определяется обработчиком запросов.

</dd> <dt>

*lParam* 
</dt> <dd>

Содержит дополнительные данные сообщения. Содержимое этого параметра определяется обработчиком запросов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение возвращаемого значения определяется обработчиком запроса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Кмнкуери. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





