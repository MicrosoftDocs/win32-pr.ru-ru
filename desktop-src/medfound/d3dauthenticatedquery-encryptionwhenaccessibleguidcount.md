---
description: Возвращает число типов шифрования, которые можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f47074947cc2f758d35691e05dda9b39f2f823feb6d647a7d77c0a3cc0030c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942764"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a>D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуидкаунт

Возвращает число типов шифрования, которые можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.



| Требование | Значение |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуидкаунт**                                                                                 |
| Входные данные  | [**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                                                         |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуидкаунт**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a>Remarks

Этот запрос поддерживают следующие типы каналов:

-   **\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**
-   **\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Запросы Защита содержимого](content-protection-queries.md)
</dt> <dt>

[Защита содержимого на основе GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




