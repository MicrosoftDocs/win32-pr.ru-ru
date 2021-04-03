---
title: DRM_Flags
description: '\_Свойство Flags DRM используется с содержимым DRM версии 1 только для указания прав, которые будут содержаться в локальной лицензии.'
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags формат Windows Media
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987191"
---
# <a name="drm_flags"></a><span data-ttu-id="82939-104">\_Флаги DRM</span><span class="sxs-lookup"><span data-stu-id="82939-104">DRM\_Flags</span></span>

<span data-ttu-id="82939-105">Свойство **\_ flags DRM** используется с содержимым DRM версии 1 только для указания прав, которые будут содержаться в локальной лицензии.</span><span class="sxs-lookup"><span data-stu-id="82939-105">The **DRM\_Flags** property is used with DRM version 1 content only to specify the rights that will be contained in the local license.</span></span> <span data-ttu-id="82939-106">Права указываются со значениями, определенными типом перечисления **\_ Rights ВМТ** .</span><span class="sxs-lookup"><span data-stu-id="82939-106">Rights are specified with values defined by the **WMT\_RIGHTS** enumeration type.</span></span> <span data-ttu-id="82939-107">Можно выбрать более одного значения, объединив их с оператором побитового **или** .</span><span class="sxs-lookup"><span data-stu-id="82939-107">More than one value can be selected by combining them with the bitwise **OR** operator.</span></span>

## <a name="global-constant"></a><span data-ttu-id="82939-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="82939-108">Global Constant</span></span>

<span data-ttu-id="82939-109">\_всзвмдрм \_ Флаги g</span><span class="sxs-lookup"><span data-stu-id="82939-109">g\_wszWMDRM\_Flags</span></span>

## <a name="data-type"></a><span data-ttu-id="82939-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="82939-110">Data Type</span></span>

<span data-ttu-id="82939-111">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="82939-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="82939-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82939-112">Remarks</span></span>

<span data-ttu-id="82939-113">При доступе к интерфейсу **IWMHeaderInfo3** объекта Writer можно добавить или изменить это значение.</span><span class="sxs-lookup"><span data-stu-id="82939-113">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="82939-114">В других объектах (редактор метаданных, читатель и синхронное средство чтения) это значение доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82939-114">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span> <span data-ttu-id="82939-115">Используйте [**ивмхеадеринфо:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , чтобы задать это свойство при создании содержимого DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="82939-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when creating DRM version 1 content.</span></span>

## <a name="see-also"></a><span data-ttu-id="82939-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82939-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82939-117">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="82939-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




