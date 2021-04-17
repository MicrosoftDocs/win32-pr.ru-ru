---
description: Указывает путь к файлу, представляющему место хранения, который модуль расшифровки содержимого (CDM) может использовать для данных, относящихся к содержимому.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542559"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>\_Свойство контентдекриптионмодуле \_ инприватесторепас MF

Указывает путь к файлу, представляющему место хранения, который модуль расшифровки содержимого (CDM) может использовать для данных, относящихся к содержимому.


## <a name="data-type"></a>Тип данных

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID свойства

**MF \_ контентдекриптионмодуле \_ инприватесторепас**

## <a name="property-value"></a>Значение свойства

Путь к файлу, который представляет место хранения. модуль расшифровки содержимого (CDM) может использоваться для данных, относящихся к содержимому.

## <a name="remarks"></a>Комментарии

Приложение должно удалить расположение хранилища после освобождения объекта CDM.

Если это свойство не задано, система будет использовать путь, указанный в свойстве [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) , для данных, относящихся к содержимому.

Задайте это свойство при создании CDM путем вызова [имфконтентдекриптионмодулеакцесс:: креатеконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Обновление Windows 10 от апреля 2020<br/>                                     |
| Header<br/>                   | <dl> <dt>мфконтентдекриптионмодуле. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

- [Свойства Media Foundation](media-foundation-properties.md)
- [Имфконтентдекриптионмодулеакцесс:: Креатеконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




