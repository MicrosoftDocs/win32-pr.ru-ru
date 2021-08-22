---
title: Значения ВТНКА (Укссеме. h)
description: Задает флаги для изменения атрибутов визуального стиля окна. Используйте одно или побитовое сочетание следующих значений.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5528e26b7dc24a744affad84c8fd1fe74607ed1af56e20651fd43723cdbbff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059294"
---
# <a name="wtnca-values"></a>Значения ВТНКА

Задает флаги для изменения атрибутов визуального стиля окна. Используйте одно или побитовое сочетание следующих значений.



| Константа/значение                                                                                                                                                                                                                                  | Описание                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <dt>**Втнка \_ НОДРАВКАПТИОН**</dt> <dt>0x00000001</dt> </dl> | Предотвращает прорисовку заголовка окна.<br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <dt>**Втнка \_ НОДРАВИКОН**</dt> <dt>0x00000002</dt> </dl>          | Предотвращает прорисовку значка системы.<br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <dt>**Втнка \_ НОСИСМЕНУ**</dt> <dt>0x00000004</dt> </dl>             | Предотвращает появление в меню системного значка.<br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <dt>**Втнка \_ НОМИРРОРХЕЛП**</dt> <dt>0x00000008</dt> </dl>    | Предотвращает зеркальное отображение вопросительного знака даже в макете с направлением письма справа налево.<br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <dt>**ВТНКА \_ валидбитс**</dt> </dl>                                                                             | Маска, которая содержит все допустимые биты.<br/>                                     |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Укссеме. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_Параметры ВТА**](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[**сетвиндовсеменонклиентаттрибутес**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





