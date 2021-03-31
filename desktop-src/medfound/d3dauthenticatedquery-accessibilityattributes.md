---
description: Возвращает тип шины ввода-вывода, используемой для отправки данных в GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423550"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a>D3DAUTHENTICATEDQUERY \_ акцессибилитяттрибутес

Возвращает тип шины ввода-вывода, используемой для отправки данных в GPU.



| Требование | Значение |
|-------------|--------------------------------------------------------------------------------------------------------------|
| GUID запроса  | **D3DAUTHENTICATEDQUERY \_ акцессибилитяттрибутес**                                                           |
| Входные данные  | [**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                         |
| Возвращать данные | [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеринфобустипе**](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a>Комментарии

Этот запрос также возвращает сведения о доступности содержимого при помещении в видеопамять.

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

 

 




