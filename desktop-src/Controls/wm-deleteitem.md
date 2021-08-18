---
title: Сообщение WM_DELETEITEM (Winuser. h)
description: Посылается владельцу списка или поля со списком при удалении списка или поля со списком, а также при удалении элементов с помощью \_ сообщения делетестринг, балансировки нагрузки \_ РЕСЕТКОНТЕНТ, CB \_ делетестринг или CB \_ ресетконтент.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- элементы управления Windows сообщений WM_DELETEITEM
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f461b63d751822d9a4c602993314bf0677cff754881269ab44458ab17f3a439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018542"
---
# <a name="wm_deleteitem-message"></a>\_Сообщение DELETEITEM WM

Посылается владельцу списка или поля со списком при удалении списка или поля со списком, а также при удалении элементов с помощью сообщения [**\_ делетестринг**](lb-deletestring.md), [**балансировки нагрузки \_ Ресетконтент**](lb-resetcontent.md), [**CB \_ делетестринг**](cb-deletestring.md)или [**CB \_ ресетконтент**](cb-resetcontent.md) . Система отправляет сообщение **WM \_ DELETEITEM** для каждого удаленного элемента. Система отправляет сообщение **WM \_ DELETEITEM** для любого удаленного поля списка или элемента поля со списком с ненулевыми данными элемента.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает идентификатор элемента управления, который отправил сообщение **WM \_ DELETEITEM** .

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**делетеитемструкт**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) , содержащую сведения об элементе, удаленном из списка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно возвращать **значение true** , если обрабатывает это сообщение.

## <a name="remarks"></a>Remarks

Microsoft Windows NT и более поздние версии: Windows отправляет сообщение **WM \_ DELETEITEM** только для элементов, удаленных из списка, нарисованного владельцем (с помощью стиля [**фунта \_ овнердравфиксед**](list-box-styles.md) или [**фунта \_ овнердраввариабле**](list-box-styles.md) ) или поля со списком, рисуемого владельцем (с помощью [**cbs \_ овнердравфиксед**](combo-box-styles.md) или типа [**cbs \_ овнердраввариабле**](combo-box-styles.md) ).

Windows 95: Windows отправляет сообщение **WM \_ DELETEITEM** для любого удаленного поля списка или элемента поля со списком с ненулевыми данными элемента.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_ДЕЛЕТЕСТРИНГ CB**](cb-deletestring.md)
</dt> <dt>

[**\_РЕСЕТКОНТЕНТ CB**](cb-resetcontent.md)
</dt> <dt>

[**делетеитемструкт**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**делетестринг балансировки нагрузки \_**](lb-deletestring.md)
</dt> <dt>

[**ресетконтент балансировки нагрузки \_**](lb-resetcontent.md)
</dt> </dl>

 

 





