---
title: DRM_DRMHeader_KeyID
description: Атрибут DRM \_ дрмхеадер \_ KEYID содержит идентификатор ключа для файла.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID формат Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336343"
---
# <a name="drm_drmheader_keyid"></a><span data-ttu-id="56373-104">\_Дрмхеадер \_ KeyID DRM</span><span class="sxs-lookup"><span data-stu-id="56373-104">DRM\_DRMHeader\_KeyID</span></span>

<span data-ttu-id="56373-105">Атрибут **DRM \_ дрмхеадер \_ KeyID** содержит идентификатор ключа для файла.</span><span class="sxs-lookup"><span data-stu-id="56373-105">The **DRM\_DRMHeader\_KeyID** attribute contains the key ID for the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="56373-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="56373-106">Global Constant</span></span>

<span data-ttu-id="56373-107">g \_ всзвмдрм \_ дрмхеадер \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="56373-107">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="56373-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="56373-108">Data Type</span></span>

<span data-ttu-id="56373-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="56373-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="56373-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56373-110">Remarks</span></span>

<span data-ttu-id="56373-111">Этот атрибут имеется только в содержимом DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="56373-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="56373-112">Его можно получить с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="56373-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="56373-113">Чтобы задать идентификатор ключа для файла с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , необходимо использовать свойство [**\_ KeyID DRM**](drm-keyid.md) .</span><span class="sxs-lookup"><span data-stu-id="56373-113">To set the key ID on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_KeyID**](drm-keyid.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="56373-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56373-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56373-115">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="56373-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




