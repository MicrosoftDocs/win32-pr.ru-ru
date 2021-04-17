---
description: Возвращает количество защищенных общих ресурсов, которые могут быть открыты любым процессом без ограничений.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662113"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a>D3DAUTHENTICATEDQUERY \_ унрестриктедпротектедшаредресаурцекаунт

Возвращает количество защищенных общих ресурсов, которые могут быть открыты любым процессом без ограничений.



| Требование | Значение |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ унрестриктедпротектедшаредресаурцекаунт**                                                                                                    |
| Входные данные  | [**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                                                                                   |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерюнрестриктедпротектедшаредресаурцекаунт**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a>Комментарии

Единственным типом канала, поддерживающим этот запрос, является **D3DAUTHENTICATEDCHANNEL \_ Driver \_ Software**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                             |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Запросы Защита содержимого](content-protection-queries.md)
</dt> <dt>

[Защита содержимого на основе GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




