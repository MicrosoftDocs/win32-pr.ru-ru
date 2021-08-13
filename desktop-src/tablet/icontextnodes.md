---
description: Содержит коллекцию объектов, реализующих интерфейс Иконтекстноде и являющихся результатом операции анализа рукописного ввода.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Интерфейс Иконтекстнодес (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e1cc15817fa36c8cecaf06c1da0fd8fb7dae77b77909f2e04b5ebaef8100d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266154"
---
# <a name="icontextnodes-interface"></a>Интерфейс Иконтекстнодес

Содержит коллекцию объектов, реализующих интерфейс [**иконтекстноде**](icontextnode.md) и являющихся результатом операции анализа рукописного ввода.

## <a name="members"></a>Элементы

Интерфейс **иконтекстнодес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иконтекстнодес** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иконтекстнодес** содержит следующие методы.



| Метод                                                       | Описание                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**аддконтекстноде**](icontextnodes-addcontextnode.md)       | Добавляет объект [**иконтекстноде**](icontextnode.md) в эту коллекцию. <br/>                                  |
| [**жетконтекстноде**](icontextnodes-getcontextnode.md)       | Извлекает объект [**иконтекстноде**](icontextnode.md) по указанному индексу в данной коллекции. <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | Возвращает число объектов [**иконтекстноде**](icontextnode.md) , содержащихся в этой коллекции. <br/>       |
| [**ремовеконтекстноде**](icontextnodes-removecontextnode.md) | Удаляет объект [**иконтекстноде**](icontextnode.md) из этой коллекции. <br/>                             |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

