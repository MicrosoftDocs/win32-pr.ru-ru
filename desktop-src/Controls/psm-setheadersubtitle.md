---
title: Сообщение PSM_SETHEADERSUBTITLE (Пршт. h)
description: Задает текст подзаголовка для заголовка внутренней страницы мастера. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ сесеадерсубтитле.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- Элементы управления Windows для PSM_SETHEADERSUBTITLE сообщений
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
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988594"
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

## <a name="remarks"></a>Комментарии

Если указать текущую страницу, она будет немедленно перерисована для вывода нового субтитра.

> [!Note]  
> Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl>      |
| Имя в кодировке Юникод и ANSI<br/>   | **ПСМ \_ СЕСЕАДЕРСУБТИТЛЕВ** (Юникод) и **ПСМ \_ сесеадерсубтитлеа** (ANSI)<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ПСМ \_ хвндтоиндекс**](psm-hwndtoindex.md)
</dt> <dt>

[**ПСМ \_ идтоиндекс**](psm-idtoindex.md)
</dt> <dt>

[**ПСМ \_ пажетоиндекс**](psm-pagetoindex.md)
</dt> </dl>

 

 





