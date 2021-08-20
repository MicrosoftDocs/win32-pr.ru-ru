---
title: Константы ПИКТИПЕ (Олектл. h)
description: Опишите тип объекта изображения, возвращаемый типом Ипиктуре Get \_ , а также описание типа изображения в элементе пиктипе структуры пиктдеск, которая передается олекреатепиктуреиндирект.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6ac7be72ba34616a1ae8d596efbad3af761760c8f5e5c2bfa5dc8362593748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567654"
---
# <a name="pictype-constants"></a>Константы ПИКТИПЕ

Опишите тип объекта изображения, возвращаемый функцией [**ипиктуре:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), а также описание типа изображения в элементе **пиктипе** структуры [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , передаваемой [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).



| Константа/значение                                                                                                                                                                                                                                  | Описание                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**Пиктипе \_ Не ИНИЦИАЛИЗИРОВАНо**</dt> <dt>(-1)</dt> </dl> | Объект изображения в настоящее время не инициализирован. Это значение допустимо только в качестве возвращаемого значения из [**ипиктуре:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) и недопустимо для структуры [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**Пиктипе \_ НЕТ**</dt> <dt>0</dt> </dl>                               | Новый объект изображения будет создан без инициализированного состояния. Это значение допустимо только в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**Пиктипе \_ ТОЧЕЧный рисунок**</dt> <dt>1</dt> </dl>                         | Тип изображения — точечный рисунок. Если это значение встречается в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , это означает, что поле **BMP** этой структуры содержит соответствующие параметры инициализации.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**Пиктипе \_ МЕТАФАЙЛ**</dt> <dt>2</dt> </dl>                   | Тип изображения — метафайл. Если это значение встречается в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , это означает, что поле **WMF** этой структуры содержит соответствующие параметры инициализации.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**Пиктипе \_ ЗНАЧОК**</dt> <dt>3</dt> </dl>                               | Тип изображения — значок. Если это значение встречается в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , это означает, что поле **Icon** этой структуры содержит соответствующие параметры инициализации.<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**Пиктипе \_ ЕНХМЕТАФИЛЕ**</dt> <dt>4</dt> </dl>          | Тип изображения является расширенным метафайлом. Если это значение встречается в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , это означает, что поле **EMF** этой структуры содержит соответствующие параметры инициализации.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Олектл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ипиктуре:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





