---
title: IMsRdpClientAdvancedSettings8 Бандвидсдетектион, свойство
description: Указывает, будут ли изменения пропускной способности обнаружены автоматически.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Бандвидсдетектион
- Службы удаленных рабочих столов свойства Бандвидсдетектион, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Бандвидсдетектион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681806"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a><span data-ttu-id="1e584-106">Свойство IMsRdpClientAdvancedSettings8:: Бандвидсдетектион</span><span class="sxs-lookup"><span data-stu-id="1e584-106">IMsRdpClientAdvancedSettings8::BandwidthDetection property</span></span>

<span data-ttu-id="1e584-107">Указывает, будут ли изменения пропускной способности обнаружены автоматически.</span><span class="sxs-lookup"><span data-stu-id="1e584-107">Specifies if bandwidth changes are automatically detected.</span></span>

<span data-ttu-id="1e584-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1e584-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e584-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e584-109">Syntax</span></span>


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a><span data-ttu-id="1e584-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1e584-110">Property value</span></span>

<span data-ttu-id="1e584-111">**Вариант \_ Значение TRUE** , если изменения пропускной способности обнаруживаются автоматически или **Variant \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1e584-111">**VARIANT\_TRUE** if bandwidth changes are automatically detected or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e584-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1e584-112">Requirements</span></span>



| <span data-ttu-id="1e584-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1e584-113">Requirement</span></span> | <span data-ttu-id="1e584-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1e584-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e584-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e584-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1e584-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1e584-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="1e584-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e584-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1e584-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e584-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="1e584-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1e584-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e584-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e584-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e584-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1e584-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e584-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e584-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e584-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e584-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e584-124">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1e584-124">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





