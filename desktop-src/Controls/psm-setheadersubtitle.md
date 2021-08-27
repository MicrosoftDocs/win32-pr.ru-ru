---
title: Сообщение PSM_SETHEADERSUBTITLE (Пршт. h)
description: Задает текст подзаголовка для заголовка внутренней страницы мастера. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ сесеадерсубтитле.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- элементы управления Windows сообщений PSM_SETHEADERSUBTITLE
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e030b75a933ba7f647f8b3dffa5e45637999d45f3299f8280fd1db3afb9857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088504"
---
# <a name="psm_setheadersubtitle-message"></a>\_Сообщение ПСМ сесеадерсубтитле

Задает текст подзаголовка для заголовка внутренней страницы мастера. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ сесеадерсубтитле**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс страницы мастера.

</dd> <dt>

*lParam* 
</dt> <dd>

Подзаголовок нового заголовка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Если указать текущую страницу, она будет немедленно перерисована для вывода нового субтитра.

> [!Note]  
> Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl>      |
| Имя в кодировке Юникод и ANSI<br/>   | **ПСМ \_ СЕСЕАДЕРСУБТИТЛЕВ** (Юникод) и **ПСМ \_ сесеадерсубтитлеа** (ANSI)<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ПСМ \_ хвндтоиндекс**](psm-hwndtoindex.md)
</dt> <dt>

[**ПСМ \_ идтоиндекс**](psm-idtoindex.md)
</dt> <dt>

[**ПСМ \_ пажетоиндекс**](psm-pagetoindex.md)
</dt> </dl>

 

 





