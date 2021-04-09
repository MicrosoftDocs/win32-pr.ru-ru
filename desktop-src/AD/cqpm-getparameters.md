---
title: Сообщение CQPM_GETPARAMETERS (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок на странице расширения формы запроса для получения данных о запросе, выполняемом страницей.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_GETPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891565"
---
# <a name="cqpm_getparameters-message"></a>\_Сообщение ККПМ Parameters

Сообщение **ККПМ \_ Parameters** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса для получения данных о запросе, выполняемом страницей.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на значение [**лпдскуерипарамс**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) , которое получает данные о запросе, выполняемом страницей. Если этот параметр имеет **значение NULL**, то расширение структуры **дскуерипарамс** должно быть выделено расширением с помощью функции [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .

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
</dt> <dt>

[**дскуерипарамс**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

