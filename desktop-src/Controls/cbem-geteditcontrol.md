---
title: Сообщение CBEM_GETEDITCONTROL (Коммктрл. h)
description: Возвращает маркер для элемента управления "поле ввода" элемента управления ComboBoxEx. Элемент управления ComboBoxEx использует поле ввода, если для него задан \_ стиль раскрывающегося списка CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- Элементы управления Windows для CBEM_GETEDITCONTROL сообщений
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
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137178"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





