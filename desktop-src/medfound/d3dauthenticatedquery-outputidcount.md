---
description: Возвращает число идентификаторов вывода, связанных с указанным сеансом шифрования и устройством Direct3D.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808117"
---
# <a name="d3dauthenticatedquery_outputidcount"></a>D3DAUTHENTICATEDQUERY \_ аутпутидкаунт

Возвращает число идентификаторов вывода, связанных с указанным сеансом шифрования и устройством Direct3D.



| Требование | Значение |
|-------------|------------------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**                                                                         |
| Входные данные  | [**\_ \_ Входные данные куерйоутпутидкаунт D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерйоутпутидкаунт**](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a>Комментарии

Этот запрос поддерживают следующие типы каналов:

-   **\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**
-   **\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**

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

 

 




