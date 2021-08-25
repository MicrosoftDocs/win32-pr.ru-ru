---
description: Следующие GUID поддерживают реализации модуля расшифровки содержимого (CDM).
title: Глобальные уникальные идентификаторы модуля расшифровки контента (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: ef4016b731b492ed61c6aed859a905446de72c308e03a734aa3cc8f573645668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958784"
---
# <a name="content-decryption-module-cdm-guids"></a>Глобальные уникальные идентификаторы модуля расшифровки контента (CDM)

Следующие GUID поддерживают реализации модуля расшифровки содержимого (CDM).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

Идентификатор GUID службы, используемый для получения интерфейсов из реализации [имфконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , такой как интерфейс WinRT [имедиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver) . Реализация **имфконтентдекриптионмодуле** должна реализовывать [имфжетсервице](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) и поддерживать этот идентификатор GUID службы.


## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>мфконтентдекриптионмодуле. h</dt> </dl> |



## <a name="see-also"></a>См. также



- [Константы Media Foundation](media-foundation-constants.md)
- [Имфконтентдекриптионмодуле] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [имедиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [имфжетсервице](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




