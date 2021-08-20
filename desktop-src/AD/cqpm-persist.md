---
title: Сообщение CQPM_PERSIST (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок страницы расширения формы запроса, чтобы разрешить странице считывать или записывать данные запросов из энергонезависимой памяти.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_PERSIST Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66eeeba5f80397aa422c465cb224064c58a4544f4d64ae2fba3bed5030b1c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020974"
---
# <a name="cqpm_persist-message"></a>ККПМ \_ сообщение о сохранении

Сообщение **о \_ сохранении ККПМ** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса, чтобы разрешить странице считывать или записывать данные запросов из энергонезависимой памяти.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Содержит ненулевое значение для чтения данных запроса или нуля для записи данных запроса.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на интерфейс [**иперсисткуери**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) , в который должны считываться или записываться данные запроса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение \_ ОК** , если успешно, или стандартный код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>Кмнкуери. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**иперсисткуери**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

