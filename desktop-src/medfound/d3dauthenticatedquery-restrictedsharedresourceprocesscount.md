---
description: Возвращает число процессов, которым разрешено открывать общие ресурсы с ограниченным доступом.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 59ba86a372a7cb505b5b9b3b6a980abbb4de4143f699a44bca015879bea62af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064441"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a>D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесскаунт

Возвращает число процессов, которым разрешено открывать общие ресурсы с ограниченным доступом.



| Требование | Значение |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесскаунт**                                                                                                |
| Входные данные  | [**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                                                                           |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесскаунт**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a>Remarks

Этот запрос поддерживают следующие типы каналов:

-   **D3DAUTHENTICATEDCHANNEL \_ d3d9**
-   **\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**

## <a name="requirements"></a>Требования



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

 

 




