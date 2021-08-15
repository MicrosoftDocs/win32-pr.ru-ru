---
title: Сообщение CBEM_GETEDITCONTROL (Коммктрл. h)
description: Возвращает маркер для элемента управления "поле ввода" элемента управления ComboBoxEx. Элемент управления ComboBoxEx использует поле ввода, если для него задан \_ стиль раскрывающегося списка CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- элементы управления Windows сообщений CBEM_GETEDITCONTROL
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a90a1b37fab7cd8e4a492bd00ad349f96202e13ee25a404f7f4aa41f623e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414074"
---
# <a name="cbem_geteditcontrol-message"></a>\_Сообщение кбем жетедитконтрол

Возвращает маркер для элемента управления "поле ввода" элемента управления ComboBoxEx. Элемент управления ComboBoxEx использует поле ввода, если для него задан стиль [**\_ раскрывающегося списка CBS**](combo-box-styles.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер элемента управления "поле ввода" в элементе управления ComboBoxEx, если он использует стиль [**\_ раскрывающегося списка CBS**](combo-box-styles.md) . В противном случае сообщение возвращает **значение NULL**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





