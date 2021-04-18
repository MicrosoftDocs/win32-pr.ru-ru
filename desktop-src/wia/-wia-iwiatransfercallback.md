---
description: Интерфейс Ивиатрансферкаллбакк принимает обратные вызовы во время обмена данными.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Интерфейс Ивиатрансферкаллбакк (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145391"
---
# <a name="iwiatransfercallback-interface"></a>Интерфейс Ивиатрансферкаллбакк

Интерфейс **ивиатрансферкаллбакк** принимает обратные вызовы во время обмена данными.

## <a name="members"></a>Элементы

Интерфейс **ивиатрансферкаллбакк** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Ивиатрансферкаллбакк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивиатрансферкаллбакк** содержит следующие методы.



| Метод                                                                 | Описание                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**жетнекстстреам**](-wia-iwiatransfercallback-getnextstream.md)       | Возвращает новый поток для указанного элемента. <br/>                    |
| [**трансферкаллбакк**](-wia-iwiatransfercallback-transfercallback.md) | Предоставляет ход выполнения и другие уведомления во время перемещения. <br/> |



 

## <a name="remarks"></a>Комментарии

Разработчики фильтра обработки изображений должны реализовать этот интерфейс и интерфейс [**ивиаимажефилтер**](-wia-iwiaimagefilter.md) .

Интерфейс **ивиатрансферкаллбакк** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



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



 

 
