---
title: Интерфейс Ивмдрмпровидер
description: Интерфейс Ивмдрмпровидер предоставляет метод, который создает другие объекты расширенных API-интерфейсов клиента DRM Microsoft Windows Media. Вы можете получить указатель на экземпляр этого интерфейса, вызвав функцию Вмдрмкреатепровидер.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Формат Windows Media в интерфейсе Ивмдрмпровидер
- Ивмдрмпровидер интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793062"
---
# <a name="iwmdrmprovider-interface"></a>Интерфейс Ивмдрмпровидер

Интерфейс **ивмдрмпровидер** предоставляет метод, который создает другие объекты расширенных API-интерфейсов клиента DRM Microsoft Windows Media.

Указатель на экземпляр этого интерфейса можно получить, вызвав функцию [**вмдрмкреатепровидер**](wmdrmcreateprovider.md) . Чтобы получить указатель на экземпляр этого интерфейса, который может создавать защищенные объекты, необходимо вызвать функцию [**вмдрмкреатепротектедпровидер**](wmdrmcreateprotectedprovider.md) .

## <a name="members"></a>Элементы

Интерфейс **ивмдрмпровидер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ивмдрмпровидер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивмдрмпровидер** содержит следующие методы.



| Метод                                              | Описание                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**CreateObject**](iwmdrmprovider-createobject.md) | Извлекает указатель на указанный интерфейс, создавая реализующий объект при необходимости.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы**](drm-interfaces.md)
</dt> </dl>

 

