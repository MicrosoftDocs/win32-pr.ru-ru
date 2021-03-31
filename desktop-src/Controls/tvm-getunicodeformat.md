---
title: Сообщение TVM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или использовать \_ макрос Жетуникодеформат TreeView.
ms.assetid: d95f61b6-9ec1-4471-b24b-efe141428747
keywords:
- Элементы управления Windows для TVM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- TVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88478d30e8da98ebf2e2325d6152087a14bc066a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071363"
---
# <a name="tvm_getunicodeformat-message"></a>\_Сообщение TVM жетуникодеформат

Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или использовать макрос [**\_ жетуникодеформат TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает флаг формата Юникода для элемента управления. Если это значение не равно нулю, то элемент управления использует символы Юникода. Если это значение равно нулю, то элемент управления использует символы ANSI.

## <a name="remarks"></a>Комментарии

Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ сетуникодеформат**](tvm-setunicodeformat.md)
</dt> </dl>

 

 





