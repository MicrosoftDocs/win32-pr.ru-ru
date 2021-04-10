---
title: Код уведомления NM_GETCUSTOMSPLITRECT (Коммктрл. h)
description: Отправляется элементом управления "Кнопка" в родительский элемент, чтобы получить измерения для двух прямоугольников разворачивающейся кнопки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135114"
---
# <a name="nm_getcustomsplitrect-notification-code"></a>\_Код уведомления жеткустомсплитрект (NM)

Отправляется элементом управления "Кнопка" в родительский элемент, чтобы получить измерения для двух прямоугольников разворачивающейся кнопки. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на [**нмкустомсплитректинфо**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) для получения сведений об ограничивающих прямоугольниках. Структура **нмкустомсплитректинфо** отправляется с кодом уведомления как запрос для родителя, чтобы предоставить измерения для прямоугольников разворачивающейся кнопки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращайте [**кдрф \_ скипдефаулт**](cdrf-constants.md) , чтобы указать элементу управления "Кнопка" использовать значения, возвращаемые в структуре [**нмкустомсплитректинфо**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; в противном случае возвратите [**кдрф \_ додефаулт**](cdrf-constants.md).

## <a name="remarks"></a>Комментарии

Этот код уведомления отправляется элементом управления "Кнопка" перед его прорисовкой. Кнопка должна иметь тип [**\_ SPLITBUTTON**](button-styles.md) или [**BS \_ дефсплитбуттон**](button-styles.md). Если прямоугольники, возвращаемые элементу управления в *lParam* , недопустимы, они игнорируются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





