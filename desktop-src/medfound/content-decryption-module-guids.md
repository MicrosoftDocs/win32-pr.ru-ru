---
description: Следующие GUID поддерживают реализации модуля расшифровки содержимого (CDM).
title: Глобальные уникальные идентификаторы модуля расшифровки контента (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721027"
---
# <a name="content-decryption-module-cdm-guids"></a>Глобальные уникальные идентификаторы модуля расшифровки контента (CDM)

Следующие GUID поддерживают реализации модуля расшифровки содержимого (CDM).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

Идентификатор GUID службы, используемый для получения интерфейсов из реализации [имфконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , такой как интерфейс WinRT [имедиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver) . Реализация **имфконтентдекриптионмодуле** должна реализовывать [имфжетсервице](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) и поддерживать этот идентификатор GUID службы.


## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>мфконтентдекриптионмодуле. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел



- [Константы Media Foundation](media-foundation-constants.md)
- [Имфконтентдекриптионмодуле] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [имедиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [имфжетсервице](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




