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
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071567"
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
| Header<br/>                   | <dl> <dt>Кмнкуери. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**иперсисткуери**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

