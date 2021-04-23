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
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a><span data-ttu-id="45a8f-103">\_Свойство контентдекриптионмодуле \_ инприватесторепас MF</span><span class="sxs-lookup"><span data-stu-id="45a8f-103">MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH property</span></span>

<span data-ttu-id="45a8f-104">Указывает путь к файлу, представляющему место хранения, который модуль расшифровки содержимого (CDM) может использовать для данных, относящихся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="45a8f-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>


## <a name="data-type"></a><span data-ttu-id="45a8f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="45a8f-105">Data type</span></span>

<span data-ttu-id="45a8f-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="45a8f-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="45a8f-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="45a8f-107">Property GUID</span></span>

<span data-ttu-id="45a8f-108">**MF \_ контентдекриптионмодуле \_ инприватесторепас**</span><span class="sxs-lookup"><span data-stu-id="45a8f-108">**MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="45a8f-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="45a8f-109">Property value</span></span>

<span data-ttu-id="45a8f-110">Путь к файлу, который представляет место хранения. модуль расшифровки содержимого (CDM) может использоваться для данных, относящихся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="45a8f-110">A file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>

## <a name="remarks"></a><span data-ttu-id="45a8f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45a8f-111">Remarks</span></span>

<span data-ttu-id="45a8f-112">Приложение должно удалить расположение хранилища после освобождения объекта CDM.</span><span class="sxs-lookup"><span data-stu-id="45a8f-112">The app should delete the store location after the CDM object has been released.</span></span>

<span data-ttu-id="45a8f-113">Если это свойство не задано, система будет использовать путь, указанный в свойстве [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) , для данных, относящихся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="45a8f-113">If this property isn't set, the system will use the path specified with the [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) property for content-specific data.</span></span>

<span data-ttu-id="45a8f-114">Задайте это свойство при создании CDM путем вызова [имфконтентдекриптионмодулеакцесс:: креатеконтентдекриптионмодуле](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="45a8f-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="45a8f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="45a8f-115">Requirements</span></span>



| <span data-ttu-id="45a8f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="45a8f-116">Requirement</span></span> | <span data-ttu-id="45a8f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="45a8f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45a8f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45a8f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="45a8f-119">Обновление Windows 10 от апреля 2020</span><span class="sxs-lookup"><span data-stu-id="45a8f-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="45a8f-120">Header</span><span class="sxs-lookup"><span data-stu-id="45a8f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="45a8f-121"><dt>мфконтентдекриптионмодуле. h</dt></span><span class="sxs-lookup"><span data-stu-id="45a8f-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45a8f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45a8f-122">See also</span></span>

- [<span data-ttu-id="45a8f-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="45a8f-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="45a8f-124">Имфконтентдекриптионмодулеакцесс:: Креатеконтентдекриптионмодуле</span><span class="sxs-lookup"><span data-stu-id="45a8f-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




