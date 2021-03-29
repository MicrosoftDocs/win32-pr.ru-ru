---
title: Сообщение CQPM_CLEARFORM (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок запроса на страницу расширения, когда необходимо сбросить содержимое страницы до значений по умолчанию.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_CLEARFORM Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94af3a31a29da4ce5740c4e326bbf1a8961f9f82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988274"
---
# <a name="cqpm_clearform-message"></a>\_Сообщение ККПМ клеарформ

Сообщение **ККПМ \_ клеарформ** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) запроса на страницу расширения, когда необходимо сбросить содержимое страницы до значений по умолчанию.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение \_ ОК** , если успешно, или стандартный код ошибки **HRESULT** .

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

 

 





