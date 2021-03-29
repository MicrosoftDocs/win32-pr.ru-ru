---
title: Сообщение PSM_SETHEADERTITLE (Пршт. h)
description: Задает текст заголовка для заголовка внутренней страницы мастера. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ сесеадертитле.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- Элементы управления Windows для PSM_SETHEADERTITLE сообщений
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654424"
---
# <a name="psm_setheadertitle-message"></a>\_Сообщение ПСМ сесеадертитле

Задает текст заголовка для заголовка внутренней страницы мастера. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ сесеадертитле**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .

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

Если указать текущую страницу, она будет немедленно перерисована для вывода нового заголовка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ПСМ \_ СЕСЕАДЕРТИТЛЕВ** (Юникод) и **ПСМ \_ сесеадертитлеа** (ANSI)<br/>  |



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

 

 





