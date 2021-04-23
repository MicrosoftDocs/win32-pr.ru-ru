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
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a><span data-ttu-id="1e2e5-103">\_Свойство контентдекриптионмодуле \_ пмпстореконтекст MF</span><span class="sxs-lookup"><span data-stu-id="1e2e5-103">MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT property</span></span>

<span data-ttu-id="1e2e5-104">Задает строку контекста, используемую реализациями модуля расшифровки содержимого (CDM), которые используют [медиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span><span class="sxs-lookup"><span data-stu-id="1e2e5-104">Specifies a context string used by Content Decryption Module (CDM) implementations that use [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span></span>


## <a name="data-type"></a><span data-ttu-id="1e2e5-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1e2e5-105">Data type</span></span>

<span data-ttu-id="1e2e5-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="1e2e5-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1e2e5-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="1e2e5-107">Property GUID</span></span>

<span data-ttu-id="1e2e5-108">**MF \_ контентдекриптионмодуле \_ пмпстореконтекст**</span><span class="sxs-lookup"><span data-stu-id="1e2e5-108">**MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT**</span></span>

## <a name="property-value"></a><span data-ttu-id="1e2e5-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1e2e5-109">Property value</span></span>

<span data-ttu-id="1e2e5-110">Строка контекста, используемая реализациями модуля расшифровки содержимого (CDM).</span><span class="sxs-lookup"><span data-stu-id="1e2e5-110">A  a context string used by Content Decryption Module (CDM) implementations.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e2e5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e2e5-111">Remarks</span></span>

<span data-ttu-id="1e2e5-112">Разработчик CDM должен найти это значение и передать значение в [конструктор медиапротектионпмпсервер](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) , используя имя свойства "Windows. Media. Protection. пмпстореконтекст".</span><span class="sxs-lookup"><span data-stu-id="1e2e5-112">The CDM implementer should look for this value and pass the value to the [MediaProtectionPMPServer constructor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) using the property name "Windows.Media.Protection.PMPStoreContext".</span></span>


<span data-ttu-id="1e2e5-113">Приложения не должны создавать это свойство при вызове [имфконтентдекриптионмодулеакцесс:: креатеконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="1e2e5-113">Apps should not create this property when calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2e5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1e2e5-114">Requirements</span></span>



| <span data-ttu-id="1e2e5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1e2e5-115">Requirement</span></span> | <span data-ttu-id="1e2e5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1e2e5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2e5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e2e5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2e5-118">Обновление Windows 10 от апреля 2020</span><span class="sxs-lookup"><span data-stu-id="1e2e5-118">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="1e2e5-119">Header</span><span class="sxs-lookup"><span data-stu-id="1e2e5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e2e5-120"><dt>мфконтентдекриптионмодуле. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e2e5-120"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e2e5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e2e5-121">See also</span></span>

- [<span data-ttu-id="1e2e5-122">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e2e5-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="1e2e5-123">медиапротектионпмпсервер</span><span class="sxs-lookup"><span data-stu-id="1e2e5-123">MediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




