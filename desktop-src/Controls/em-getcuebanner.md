---
title: Сообщение EM_GETCUEBANNER (Коммктрл. h)
description: Возвращает текст, который отображается как текстовая подсказка или Совет в элементе управления "поле ввода".
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- элементы управления Windows сообщений EM_GETCUEBANNER
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
ms.openlocfilehash: 6e5a47811adcd13c0f2531bd645a9ea607dd68c4dd2c1154f226a54cf108b291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019722"
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

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Изменить \_ жеткуебаннертекст**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





