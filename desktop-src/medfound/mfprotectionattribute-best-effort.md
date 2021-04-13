---
description: Задайте в качестве атрибута для объекта Имфаутпутсчема.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: Атрибут MFPROTECTIONATTRIBUTE_BEST_EFFORT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263898"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a><span data-ttu-id="95c0f-103">МФПРОТЕКТИОНАТТРИБУТЕный \_ атрибут с наилучшими \_ усилиями</span><span class="sxs-lookup"><span data-stu-id="95c0f-103">MFPROTECTIONATTRIBUTE\_BEST\_EFFORT attribute</span></span>

<span data-ttu-id="95c0f-104">Задайте в качестве атрибута для объекта [**имфаутпутсчема**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="95c0f-104">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span> <span data-ttu-id="95c0f-105">Если этот атрибут имеется, неудачная попытка применения защиты игнорируется.</span><span class="sxs-lookup"><span data-stu-id="95c0f-105">If this attribute is present, a failed attempt to apply the protection is ignored.</span></span> <span data-ttu-id="95c0f-106">Если значение связанного атрибута равно **true**, следует применить схему защиты с атрибутом [мфпротектионаттрибуте \_ отработки отказа \_](mfprotectionattribute-fail-over.md) .</span><span class="sxs-lookup"><span data-stu-id="95c0f-106">If the associated attribute value is **TRUE**, the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute should be applied.</span></span>

## <a name="data-type"></a><span data-ttu-id="95c0f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="95c0f-107">Data type</span></span>

<span data-ttu-id="95c0f-108">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="95c0f-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="95c0f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95c0f-109">Remarks</span></span>

<span data-ttu-id="95c0f-110">Если **значение — true**, принудительно Примените схему защиты с атрибутом [мфпротектионаттрибуте \_ \_ отработки отказа](mfprotectionattribute-fail-over.md) , если установить эту защиту не удается.</span><span class="sxs-lookup"><span data-stu-id="95c0f-110">If **TRUE**, enforce the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute if setting this protection fails.</span></span>

<span data-ttu-id="95c0f-111">Задайте в качестве атрибута для объекта [**имфаутпутсчема**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="95c0f-111">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="95c0f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="95c0f-112">Requirements</span></span>



| <span data-ttu-id="95c0f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="95c0f-113">Requirement</span></span> | <span data-ttu-id="95c0f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="95c0f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95c0f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95c0f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="95c0f-116">\[Только приложения UWP Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="95c0f-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="95c0f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95c0f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="95c0f-118">Только приложения UWP для Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="95c0f-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="95c0f-119">Header</span><span class="sxs-lookup"><span data-stu-id="95c0f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="95c0f-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c0f-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95c0f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95c0f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c0f-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95c0f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="95c0f-123">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="95c0f-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




