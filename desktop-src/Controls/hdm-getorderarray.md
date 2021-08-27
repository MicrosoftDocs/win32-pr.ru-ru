---
title: Сообщение HDM_GETORDERARRAY (Коммктрл. h)
description: Возвращает текущий порядок элементов в элементе управления "заголовок" слева направо. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса жетордераррай.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- элементы управления Windows сообщений HDM_GETORDERARRAY
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f374424fe3f1d84c4919c26948486a9bae1660072975556aecaac4b08b85b33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062834"
---
# <a name="hdm_getorderarray-message"></a>\_Сообщение ЖЕТОРДЕРАРРАЙ HDM

Возвращает текущий порядок элементов в элементе управления "заголовок" слева направо. Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ жетордераррай**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Число целочисленных элементов, которые может содержать *lParam* . Это значение должно быть равно числу элементов в элементе управления (см. раздел [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив целых чисел, получающий значения индекса для элементов в заголовке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха, и буфер в *lParam* получает номер элемента для каждого элемента в элементе управления "заголовок" в том порядке, в котором они отображаются слева направо. В противном случае сообщение возвращает ноль.

## <a name="remarks"></a>Remarks

Число элементов в параметре *lParam* указывается в параметре *wParam* и должно быть равно числу элементов в элементе управления. Например, следующий фрагмент кода зарезервирует достаточно памяти для хранения значений индекса.


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





