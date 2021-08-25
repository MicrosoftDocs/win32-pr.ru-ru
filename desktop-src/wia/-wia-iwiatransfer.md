---
description: Интерфейс Ивиатрансфер обеспечивает передачу данных на основе потока.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Интерфейс Ивиатрансфер (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: ff19619b1f0ab46658d0876792248befd6940c525d5c7da1b3331f6ca1a8c12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813904"
---
# <a name="iwiatransfer-interface"></a>Интерфейс Ивиатрансфер

Интерфейс **ивиатрансфер** обеспечивает передачу данных на основе потока.

## <a name="members"></a>Элементы

Интерфейс **ивиатрансфер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Ивиатрансфер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивиатрансфер** содержит следующие методы.



| Метод                                                                 | Описание                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Отменить**](-wia-iwiatransfer-cancel.md)                             | Отменяет текущую операцию перемещения. <br/>                                         |
| [**Загрузка**](-wia-iwiatransfer-download.md)                         | Инициирует загрузку данных в вызывающий объект. <br/>                                        |
| [**\_ \_ Сведения о формате енумвиа**](-wia-iwiatransfer-enumwia-format-info.md) | Создает перечислитель для форматов перемещения, поддерживаемых устройством WIA 2,0.<br/> |
| [**Передать**](-wia-iwiatransfer-upload.md)                             | Инициирует отправку данных одного элемента от вызывающего. <br/>                       |



 

## <a name="remarks"></a>Remarks

Интерфейс **ивиатрансфер** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Методы IUnknown                                        | Описание                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Возвращает указатели на поддерживаемые интерфейсы. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Увеличивает значение счетчика ссылок.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Уменьшает значение счетчика ссылок.               |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 
