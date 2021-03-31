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
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263130"
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
| [**Скачать**](-wia-iwiatransfer-download.md)                         | Инициирует загрузку данных в вызывающий объект. <br/>                                        |
| [**\_ \_ Сведения о формате енумвиа**](-wia-iwiatransfer-enumwia-format-info.md) | Создает перечислитель для форматов перемещения, поддерживаемых устройством WIA 2,0.<br/> |
| [**Передать**](-wia-iwiatransfer-upload.md)                             | Инициирует отправку данных одного элемента от вызывающего. <br/>                       |



 

## <a name="remarks"></a>Комментарии

Интерфейс **ивиатрансфер** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Методы IUnknown                                        | Описание                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Возвращает указатели на поддерживаемые интерфейсы. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Увеличивает значение счетчика ссылок.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Уменьшает значение счетчика ссылок.               |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 
