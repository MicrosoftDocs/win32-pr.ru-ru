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
# <a name="mf_contentdecryptionmodule_storepath-property"></a><span data-ttu-id="da955-103">\_Свойство контентдекриптионмодуле \_ Требуется StorePath MF</span><span class="sxs-lookup"><span data-stu-id="da955-103">MF\_CONTENTDECRYPTIONMODULE\_STOREPATH property</span></span>

<span data-ttu-id="da955-104">Указывает путь к файлу, представляющему место хранения, которое модуль расшифровки содержимого (CDM) может использовать для инициализации.</span><span class="sxs-lookup"><span data-stu-id="da955-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>


## <a name="data-type"></a><span data-ttu-id="da955-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="da955-105">Data type</span></span>

<span data-ttu-id="da955-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="da955-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="da955-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="da955-107">Property GUID</span></span>

<span data-ttu-id="da955-108">**MF \_ контентдекриптионмодуле \_ Требуется StorePath**</span><span class="sxs-lookup"><span data-stu-id="da955-108">**MF\_CONTENTDECRYPTIONMODULE\_STOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="da955-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="da955-109">Property value</span></span>

<span data-ttu-id="da955-110">Путь к файлу, представляющий место хранения, которое модуль расшифровки содержимого (CDM) может использовать для инициализации.</span><span class="sxs-lookup"><span data-stu-id="da955-110">A file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>

## <a name="remarks"></a><span data-ttu-id="da955-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da955-111">Remarks</span></span>

<span data-ttu-id="da955-112">Путь, указанный с помощью этого свойства, также будет использоваться для данных, связанных с содержимым, если не задано свойство [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) .</span><span class="sxs-lookup"><span data-stu-id="da955-112">The path specified with this property will also be used for content-specific data if the [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) property isn't set.</span></span>

<span data-ttu-id="da955-113">Чтобы повысить производительность COM, приложение не должно удалять место хранения после освобождения объекта CDM.</span><span class="sxs-lookup"><span data-stu-id="da955-113">To improve COM performance, the app should not delete the store location after the CDM object has been released.</span></span>



<span data-ttu-id="da955-114">Задайте это свойство при создании CDM путем вызова [имфконтентдекриптионмодулеакцесс:: креатеконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="da955-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="da955-115">Требования</span><span class="sxs-lookup"><span data-stu-id="da955-115">Requirements</span></span>



| <span data-ttu-id="da955-116">Требование</span><span class="sxs-lookup"><span data-stu-id="da955-116">Requirement</span></span> | <span data-ttu-id="da955-117">Значение</span><span class="sxs-lookup"><span data-stu-id="da955-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da955-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da955-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da955-119">Обновление Windows 10 от апреля 2020</span><span class="sxs-lookup"><span data-stu-id="da955-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="da955-120">Header</span><span class="sxs-lookup"><span data-stu-id="da955-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="da955-121"><dt>мфконтентдекриптионмодуле. h</dt></span><span class="sxs-lookup"><span data-stu-id="da955-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da955-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da955-122">See also</span></span>

- [<span data-ttu-id="da955-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da955-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="da955-124">Имфконтентдекриптионмодулеакцесс:: Креатеконтентдекриптионмодуле</span><span class="sxs-lookup"><span data-stu-id="da955-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




