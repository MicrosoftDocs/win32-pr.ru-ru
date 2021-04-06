---
description: Содержит коллекцию объектов, реализующих интерфейс Иконтекстлинк.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Интерфейс Иконтекстлинкс (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991163"
---
# <a name="icontextlinks-interface"></a>Интерфейс Иконтекстлинкс

Содержит коллекцию объектов, реализующих интерфейс [**иконтекстлинк**](icontextlink.md) .

## <a name="members"></a>Элементы

Интерфейс **иконтекстлинкс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иконтекстлинкс** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иконтекстлинкс** содержит следующие методы.



| Метод                                                 | Описание                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**жетконтекстлинк**](icontextlinks-getcontextlink.md) | Извлекает [**иконтекстлинк**](icontextlink.md) по указанному индексу.<br/>               |
| [**GetCount**](icontextlinks-getcount.md)             | Возвращает число объектов [**иконтекстлинк**](icontextlink.md) в данной коллекции.<br/> |



 

## <a name="remarks"></a>Комментарии

Доступ к этому методу обычно осуществляется с помощью метода [**иконтекстноде:: жетконтекстлинкс**](icontextnode-getcontextlinks.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстлинк**](icontextlink.md)
</dt> <dt>

[**Иконтекстноде:: Аддконтекстлинк**](icontextnode-addcontextlink.md)
</dt> <dt>

[**Иконтекстноде::D Елетеконтекстлинк**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**Иконтекстноде:: Жетконтекстлинкс**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

