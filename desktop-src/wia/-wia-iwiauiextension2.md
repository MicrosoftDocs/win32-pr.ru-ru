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
ms.openlocfilehash: 2111c25a83a9b826f4cab7dba8f689e01a9868ac416b8fb3026f1b1fb49a90ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208147"
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



 

## <a name="remarks"></a>Remarks



| Методы IUnknown                                        | Описание                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Возвращает указатели на поддерживаемые интерфейсы. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Увеличивает значение счетчика ссылок.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Уменьшает значение счетчика ссылок.               |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Виадевд. h</dt> </dl> |



 

 
