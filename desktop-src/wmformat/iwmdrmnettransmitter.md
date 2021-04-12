---
title: Интерфейс Ивмдрмнеттрансмиттер
description: Интерфейс Ивмдрмнеттрансмиттер предоставляет методы, необходимые для использования Windows Media DRM для сетевых устройств в качестве передатчика. Чтобы получить экземпляр этого интерфейса, вызовите Ивмдрмпровидер CreateObject. Передайте IID \_ ивмдрмнеттрансмиттер в качестве параметра riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Формат Windows Media в интерфейсе Ивмдрмнеттрансмиттер
- Ивмдрмнеттрансмиттер интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338300"
---
# <a name="iwmdrmnettransmitter-interface"></a>Интерфейс Ивмдрмнеттрансмиттер

Интерфейс **ивмдрмнеттрансмиттер** предоставляет методы, необходимые для использования Windows Media DRM для сетевых устройств в качестве передатчика.

Чтобы получить экземпляр этого интерфейса, вызовите метод [**ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md). Передайте **IID \_ ивмдрмнеттрансмиттер** в качестве параметра *riid* .

## <a name="members"></a>Элементы

Интерфейс **ивмдрмнеттрансмиттер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ивмдрмнеттрансмиттер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивмдрмнеттрансмиттер** содержит следующие методы.



| Метод                                                                        | Описание                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**жетлеафлиценсереспонсе**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Создает сообщение с ответом на конечную лицензию.<br/>                                                       |
| [**жетрутлиценсереспонсе**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Создает сообщение с ответом корневой лицензии<br/>                                                        |
| [**сетлиценсечалленже**](iwmdrmnettransmitter-setlicensechallenge.md)       | Обрабатывает запрос лицензии, отправленный получателем DRM Microsoft Windows Media для сетевых устройств<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы**](drm-interfaces.md)
</dt> <dt>

[**Интерфейс Ивмдрмнетрецеивер**](iwmdrmnetreceiver.md)
</dt> </dl>

 

