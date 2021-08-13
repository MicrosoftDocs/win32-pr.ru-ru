---
description: Интерфейс Ивиапревиев кэширует нефильтрованные изображения внутренним образом и передает их через фильтры обработки изображений.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Интерфейс Ивиапревиев (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e2672211e5c1a17fa360a6078069ae8260687dc896843ffb6bf572d9b7be8caa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442074"
---
# <a name="iwiapreview-interface"></a>Интерфейс Ивиапревиев

Интерфейс **ивиапревиев** кэширует нефильтрованные изображения внутренним образом и передает их через фильтры обработки изображений.

## <a name="members"></a>Элементы

Интерфейс **ивиапревиев** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Ивиапревиев** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивиапревиев** содержит следующие методы.



| Метод                                                  | Описание                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clear**](-wia-iwiapreview-clear.md)                 | Освобождает нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) . Он также освобождает фильтр обработки изображений. <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | Вызывает фильтр сегментации драйвера и передает в фильтр нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) . <br/> |
| [**жетневпревиев**](-wia-iwiapreview-getnewpreview.md) | Внутренне кэширует нефильтрованное изображение, возвращенное драйвером. <br/>                                                                                                                |
| [**упдатепревиев**](-wia-iwiapreview-updatepreview.md) | Возвращает нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) . <br/>                                                            |



 

## <a name="remarks"></a>Remarks

Этот фильтр вызывается автоматически методом [**ивиатрансфер::D гружать**](-wia-iwiatransfer-download.md) .

Интерфейс **ивиапревиев** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Методы IUnknown                                        | Описание                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Возвращает указатели на поддерживаемые интерфейсы. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Увеличивает значение счетчика ссылок.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Уменьшает значение счетчика ссылок.               |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
