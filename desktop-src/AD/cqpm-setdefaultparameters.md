---
title: Сообщение CQPM_SETDEFAULTPARAMETERS (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок на странице расширения формы запроса, чтобы задать альтернативные параметры по умолчанию для страницы.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_SETDEFAULTPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490383"
---
# <a name="cqpm_setdefaultparameters-message"></a>\_Сообщение ККПМ сетдефаултпараметерс

Сообщение **ККПМ \_ сетдефаултпараметерс** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса, чтобы задать альтернативные параметры по умолчанию для страницы.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Содержит ненулевое значение, если страница является страницей по умолчанию или ноль в противном случае.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**опенкуеривиндов**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) , содержащую данные о диалоговом окне "запрос службы каталогов".

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
</dt> <dt>

[**опенкуеривиндов**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





