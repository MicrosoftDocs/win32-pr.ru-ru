---
description: Возвращает один из идентификаторов вывода, связанный с указанным сеансом шифрования и устройством Direct3D.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808122"
---
# <a name="d3dauthenticatedquery_outputid"></a>D3DAUTHENTICATEDQUERY \_ аутпутид

Возвращает один из идентификаторов вывода, связанный с указанным сеансом шифрования и устройством Direct3D.



| Требование | Значение |
|-------------|--------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ аутпутид**                                                                    |
| Входные данные  | [**\_ \_ Входные данные куерйоутпутид D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерйоутпутид**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

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

 

 




