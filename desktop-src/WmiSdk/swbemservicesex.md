---
description: Расширяет функциональные возможности SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Объект Свбемсервицесекс (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f7b63cbf6bc048350546b431b4f967c815450abf2d79c7ba79ab8f84e562a1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107842"
---
# <a name="swbemservicesex-object"></a>Объект Свбемсервицесекс

Объект **свбемсервицесекс** расширяет функциональные возможности [**SwbemServices**](swbemservices.md). Методы [**помещения**](swbemservicesex-put.md) и [**путасинк**](swbemservicesex-putasync.md) позволяют сохранять класс или экземпляр в нескольких пространствах имен или в пространстве имен, отличном от того, где был создан экземпляр. Не удается создать этот объект с [помощью вызова функции](/previous-versions//xzysf6hc(v=vs.85)) VBScript.

## <a name="members"></a>Элементы

Объект **свбемсервицесекс** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Объект **свбемсервицесекс** содержит эти методы.



| Метод                                       | Описание                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PUT**](swbemservicesex-put.md)           | Сохраняет объект в пространство имен, привязанное к объекту **свбемсервицесекс** , и возвращает объект [**свбемобжектпас**](swbemobjectpath.md) , содержащий путь к объекту, в который были записаны данные.<br/> |
| [**путасинк**](swbemservicesex-putasync.md) | Асинхронно сохраняет объект в пространстве имен.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Remarks

Методы в этом классе могут вызываться либо в режиме семисинчронаус, либо в асинхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_ИСВБЕМСЕРВИЦЕСЕКС CLSID<br/>                                                      |
| IID<br/>                      | IID \_ исвбемсервицесекс<br/>                                                        |



## <a name="see-also"></a>См. также

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> <dt>

[Вызов метода](calling-a-method.md)
</dt> </dl>

 

