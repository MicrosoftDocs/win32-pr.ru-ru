---
title: DRM_LicenseID
description: '\_Свойство ЛИЦЕНСЕИД DRM содержит строку, полученную из лицензии, связанной с текущим открытым файлом, который однозначно идентифицирует эту лицензию.'
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID формат Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336423"
---
# <a name="drm_licenseid"></a><span data-ttu-id="d61b3-104">\_ЛИЦЕНСЕИД DRM</span><span class="sxs-lookup"><span data-stu-id="d61b3-104">DRM\_LicenseID</span></span>

<span data-ttu-id="d61b3-105">Свойство **\_ лиценсеид DRM** содержит строку, полученную из лицензии, связанной с текущим открытым файлом, который однозначно идентифицирует эту лицензию.</span><span class="sxs-lookup"><span data-stu-id="d61b3-105">The **DRM\_LicenseID** property contains a string retrieved from the license associated with the currently open file that uniquely identifies that license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d61b3-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="d61b3-106">Global Constant</span></span>

<span data-ttu-id="d61b3-107">g \_ всзвмдрм \_ лиценсеид</span><span class="sxs-lookup"><span data-stu-id="d61b3-107">g\_wszWMDRM\_LicenseID</span></span>

## <a name="data-type"></a><span data-ttu-id="d61b3-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d61b3-108">Data Type</span></span>

<span data-ttu-id="d61b3-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="d61b3-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d61b3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d61b3-110">Remarks</span></span>

<span data-ttu-id="d61b3-111">Этот атрибут имеется только в содержимом DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="d61b3-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="d61b3-112">Его можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , и его можно получить при помощи [**Ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="d61b3-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

<span data-ttu-id="d61b3-113">Идентификатор лицензии хранится в лицензии, а не в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="d61b3-113">The license ID is stored in a license, not in an ASF file.</span></span> <span data-ttu-id="d61b3-114">Каждая отдельная лицензия имеет уникальный идентификатор, который назначается генератором лицензий во время создания лицензии.</span><span class="sxs-lookup"><span data-stu-id="d61b3-114">Each individual license has a unique ID which is assigned by the license generator at the time the license is created.</span></span> <span data-ttu-id="d61b3-115">Например, если вы получаете две лицензии для одного и того же содержимого, у каждого из них будет свой атрибут Лиценсеид.</span><span class="sxs-lookup"><span data-stu-id="d61b3-115">For example, if you obtain two licenses for the same content, each one will have a different LicenseID attribute.</span></span> <span data-ttu-id="d61b3-116">Как правило, приложениям не нужно получать это значение.</span><span class="sxs-lookup"><span data-stu-id="d61b3-116">Typically, applications have no need to retrieve this value.</span></span>

## <a name="see-also"></a><span data-ttu-id="d61b3-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d61b3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d61b3-118">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="d61b3-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




