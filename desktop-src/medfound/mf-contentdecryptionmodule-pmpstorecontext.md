---
description: Задает строку контекста, используемую реализациями модуля расшифровки содержимого (CDM), которые используют Медиапротектионпмпсервер.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719450"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>\_Свойство контентдекриптионмодуле \_ пмпстореконтекст MF

Задает строку контекста, используемую реализациями модуля расшифровки содержимого (CDM), которые используют [медиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver).


## <a name="data-type"></a>Тип данных

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID свойства

**MF \_ контентдекриптионмодуле \_ пмпстореконтекст**

## <a name="property-value"></a>Значение свойства

Строка контекста, используемая реализациями модуля расшифровки содержимого (CDM).

## <a name="remarks"></a>Комментарии

Разработчик CDM должен найти это значение и передать значение в [конструктор медиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) , используя имя свойства "Windows. Media. Protection. пмпстореконтекст".


Приложения не должны создавать это свойство при вызове [имфконтентдекриптионмодулеакцесс:: креатеконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Обновление Windows 10 от апреля 2020<br/>                                     |
| Header<br/>                   | <dl> <dt>мфконтентдекриптионмодуле. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

- [Свойства Media Foundation](media-foundation-properties.md)
- [медиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




