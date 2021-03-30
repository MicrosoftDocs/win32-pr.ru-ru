---
title: Сообщение CQPM_ENABLE (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок на странице расширения формы запроса для включения или отключения страницы.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_ENABLE Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071263"
---
# <a name="cqpm_enable-message"></a>\_Сообщение о включении ККПМ

Сообщение **ККПМ \_ Enable** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса для включения или отключения страницы.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Содержит нуль для отключения страницы или ненулевого значения для включения страницы.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения игнорируется.

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

 

 





