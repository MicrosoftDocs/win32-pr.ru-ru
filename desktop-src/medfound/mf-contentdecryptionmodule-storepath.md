---
description: Указывает путь к файлу, представляющему место хранения, которое модуль расшифровки содержимого (CDM) может использовать для инициализации.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497667"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>\_Свойство контентдекриптионмодуле \_ Требуется StorePath MF

Указывает путь к файлу, представляющему место хранения, которое модуль расшифровки содержимого (CDM) может использовать для инициализации.


## <a name="data-type"></a>Тип данных

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID свойства

**MF \_ контентдекриптионмодуле \_ Требуется StorePath**

## <a name="property-value"></a>Значение свойства

Путь к файлу, представляющий место хранения, которое модуль расшифровки содержимого (CDM) может использовать для инициализации.

## <a name="remarks"></a>Комментарии

Путь, указанный с помощью этого свойства, также будет использоваться для данных, связанных с содержимым, если не задано свойство [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) .

Чтобы повысить производительность COM, приложение не должно удалять место хранения после освобождения объекта CDM.



Задайте это свойство при создании CDM путем вызова [имфконтентдекриптионмодулеакцесс:: креатеконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Обновление Windows 10 от апреля 2020<br/>                                     |
| Header<br/>                   | <dl> <dt>мфконтентдекриптионмодуле. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

- [Свойства Media Foundation](media-foundation-properties.md)
- [Имфконтентдекриптионмодулеакцесс:: Креатеконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




