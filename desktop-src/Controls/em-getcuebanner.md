---
title: Сообщение EM_GETCUEBANNER (Коммктрл. h)
description: Возвращает текст, который отображается как текстовая подсказка или Совет в элементе управления "поле ввода".
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- Элементы управления Windows для EM_GETCUEBANNER сообщений
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989334"
---
# <a name="em_getcuebanner-message"></a>\_Сообщение ЖЕТКУЕБАННЕР EM

Возвращает текст, который отображается как текстовая подсказка или Совет в элементе управления "поле ввода".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Указатель на буфер Юникода, который получает текстовый набор в качестве текстовой подсказки. Вызывающий объект отвечает за выделение буфера.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Размер буфера, на который указывает *wParam* в **вчарс**, включая завершающее **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Изменить \_ жеткуебаннертекст**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





