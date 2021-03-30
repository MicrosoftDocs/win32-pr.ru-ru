---
title: Сообщение TB_GETIDEALSIZE (Коммктрл. h)
description: Получает идеальный размер панели инструментов.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- Элементы управления Windows для TB_GETIDEALSIZE сообщений
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071250"
---
# <a name="tb_getidealsize-message"></a>\_Сообщение ЖЕТИДЕАЛСИЗЕ ТБ

Получает идеальный размер панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>**Логическое** значение, указывающее, следует ли получить идеальную высоту или ширину панели инструментов. Используйте **значение true** для получения идеальной высоты, **false** для получения идеальной ширины.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) , получающую высоту или ширину, на которой будут отображаться все кнопки. Если параметр *wParam* имеет **значение true**, допустим только элемент **CY** (Height). Если параметр *wParam* имеет **значение false**, допустим только элемент **CX** (Width).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

