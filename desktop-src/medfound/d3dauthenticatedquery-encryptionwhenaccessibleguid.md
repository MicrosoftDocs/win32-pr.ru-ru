---
description: Возвращает один из типов шифрования, который можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692052"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a>D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид

Возвращает один из типов шифрования, который можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.



| Требование | Значение |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид**                                                                            |
| Входные данные  | [**\_ \_ Входные данные куеревиктионенкриптионгуид D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуид**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

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

 

 




