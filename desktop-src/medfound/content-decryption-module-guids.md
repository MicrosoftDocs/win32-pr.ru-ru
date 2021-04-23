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
# <a name="content-decryption-module-cdm-guids"></a><span data-ttu-id="e2239-103">Глобальные уникальные идентификаторы модуля расшифровки контента (CDM)</span><span class="sxs-lookup"><span data-stu-id="e2239-103">Content Decryption Module (CDM) GUIDs</span></span>

<span data-ttu-id="e2239-104">Следующие GUID поддерживают реализации модуля расшифровки содержимого (CDM).</span><span class="sxs-lookup"><span data-stu-id="e2239-104">The following GUIDs support Content Decryption Module (CDM) implementations.</span></span>

<span data-ttu-id="e2239-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span><span class="sxs-lookup"><span data-stu-id="e2239-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span></span>

<span data-ttu-id="e2239-106">Идентификатор GUID службы, используемый для получения интерфейсов из реализации [имфконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , такой как интерфейс WinRT [имедиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver) .</span><span class="sxs-lookup"><span data-stu-id="e2239-106">Service GUID used to obtain interfaces from an [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) implementation,such as the WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) interface.</span></span> <span data-ttu-id="e2239-107">Реализация **имфконтентдекриптионмодуле** должна реализовывать [имфжетсервице](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) и поддерживать этот идентификатор GUID службы.</span><span class="sxs-lookup"><span data-stu-id="e2239-107">An implementation of **IMFContentDecryptionModule** should implement [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) and support this service GUID.</span></span>


## <a name="requirements"></a><span data-ttu-id="e2239-108">Требования</span><span class="sxs-lookup"><span data-stu-id="e2239-108">Requirements</span></span>



| <span data-ttu-id="e2239-109">Требование</span><span class="sxs-lookup"><span data-stu-id="e2239-109">Requirement</span></span> | <span data-ttu-id="e2239-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e2239-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2239-111">Header</span><span class="sxs-lookup"><span data-stu-id="e2239-111">Header</span></span><br/> | <dl> <span data-ttu-id="e2239-112"><dt>мфконтентдекриптионмодуле. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2239-112"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2239-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2239-113">See also</span></span>



- [<span data-ttu-id="e2239-114">Константы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2239-114">Media Foundation Constants</span></span>](media-foundation-constants.md)
- <span data-ttu-id="e2239-115">[Имфконтентдекриптионмодуле] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="e2239-115">[IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span></span>
- [<span data-ttu-id="e2239-116">имедиапротектионпмпсервер</span><span class="sxs-lookup"><span data-stu-id="e2239-116">IMediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [<span data-ttu-id="e2239-117">имфжетсервице</span><span class="sxs-lookup"><span data-stu-id="e2239-117">IMFGetService</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




