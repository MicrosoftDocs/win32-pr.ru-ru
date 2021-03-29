---
description: Интерфейс IWiaUIExtension2 предоставляет методы, заменяющие стандартный, предоставляемый системой пользовательский интерфейс пользовательским интерфейсом, который предоставляет настраиваемый значок устройства.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Интерфейс IWiaUIExtension2 (Виадевд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991156"
---
# <a name="iwiauiextension2-interface"></a>Интерфейс IWiaUIExtension2

Интерфейс IWiaUIExtension2 предоставляет методы, заменяющие стандартный, предоставляемый системой пользовательский интерфейс пользовательским интерфейсом, который предоставляет настраиваемый значок устройства. Поставщики устройств могут реализовать этот интерфейс для предоставления настраиваемых пользовательских интерфейсов для своих устройств.

## <a name="members"></a>Элементы

Интерфейс **IWiaUIExtension2** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaUIExtension2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IWiaUIExtension2** содержит следующие методы.



| Метод                                                       | Описание                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**девицедиалог**](-wia-iwiauiextension2-devicedialog.md)   | Предоставляет настраиваемый пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.<br/> |
| [**жетдевицеикон**](-wia-iwiauiextension2-getdeviceicon.md) | Возвращает пользовательский значок устройства.<br/>                                                        |



 

## <a name="remarks"></a>Комментарии



| Методы IUnknown                                        | Описание                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Возвращает указатели на поддерживаемые интерфейсы. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Увеличивает значение счетчика ссылок.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Уменьшает значение счетчика ссылок.               |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Виадевд. h</dt> </dl> |



 

 
