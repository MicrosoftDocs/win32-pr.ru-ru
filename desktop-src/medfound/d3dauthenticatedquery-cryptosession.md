---
description: Возвращает дескрипторы криптографического сеанса и устройства Direct3D, связанные с указанным устройством декодера DirectX Video Acceleration 2 (ДКСВА-2).
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e824514c3fef4e3e036b8f2973d3a958c4e135ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262799"
---
# <a name="d3dauthenticatedquery_cryptosession"></a>D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION

Возвращает дескрипторы криптографического сеанса и устройства Direct3D, связанные с указанным устройством декодера DirectX Video Acceleration 2 (ДКСВА-2).



| Требование | Значение |
|-------------|------------------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**                                                                         |
| Входные данные  | [**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                             |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерикриптосессион**](d3dauthenticatedchannel-querycryptosession-output.md) |



 

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

 

 




