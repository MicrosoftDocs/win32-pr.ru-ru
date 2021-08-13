---
description: Возвращает тип шифрования, который применяется до того, как содержимое становится доступным для ЦП или шины.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 483058e8b76b7a08929e905b642338c9e8f6aa6a59128907bccfcc1f2b3856f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742624"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a>D3DAUTHENTICATEDQUERY \_ куррентенкриптионвхенакцессибле

Возвращает тип шифрования, который применяется до того, как содержимое становится доступным для ЦП или шины.



| Требование | Значение |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ куррентенкриптионвхенакцессибле**                                                                                   |
| Входные данные  | [**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                                                         |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерюнкомпресседенкриптионлевел**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a>Remarks

Этот запрос поддерживают следующие типы каналов:

-   **\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**
-   **\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Запросы Защита содержимого](content-protection-queries.md)
</dt> <dt>

[Защита содержимого на основе GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




