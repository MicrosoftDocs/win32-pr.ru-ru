---
title: IMsRdpDeviceV2 Дривелеттербитмап, свойство
description: Содержит битовое значение, представляющее собой карту букв диска, содержащихся в устройстве.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дривелеттербитмап
- Службы удаленных рабочих столов свойства Дривелеттербитмап, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Дривелеттербитмап
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801145"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a><span data-ttu-id="e8ef8-106">IMsRdpDeviceV2: свойство Ривелеттербитмап:D</span><span class="sxs-lookup"><span data-stu-id="e8ef8-106">IMsRdpDeviceV2::DriveLetterBitmap property</span></span>

<span data-ttu-id="e8ef8-107">Содержит битовое значение, представляющее собой карту букв диска, содержащихся в устройстве.</span><span class="sxs-lookup"><span data-stu-id="e8ef8-107">Contains a bitfield that represents a map of drive letters contained within the device.</span></span>

<span data-ttu-id="e8ef8-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e8ef8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ef8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8ef8-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="e8ef8-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e8ef8-110">Property value</span></span>

<span data-ttu-id="e8ef8-111">Схема букв диска, содержащихся на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e8ef8-111">A map of drive letters contained within the device.</span></span> <span data-ttu-id="e8ef8-112">Каждый бит в значении представляет букву диска.</span><span class="sxs-lookup"><span data-stu-id="e8ef8-112">Each bit in the value represents a drive letter.</span></span> <span data-ttu-id="e8ef8-113">Младший значащий бит представляет букву диска "A", следующий бит представляет букву диска "B" и т. д.</span><span class="sxs-lookup"><span data-stu-id="e8ef8-113">The least significant bit represents drive letter "A", the next bit represents drive letter "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8ef8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e8ef8-114">Requirements</span></span>



| <span data-ttu-id="e8ef8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e8ef8-115">Requirement</span></span> | <span data-ttu-id="e8ef8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e8ef8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ef8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8ef8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ef8-118">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="e8ef8-118">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="e8ef8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8ef8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ef8-120">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="e8ef8-120">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="e8ef8-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e8ef8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8ef8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8ef8-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8ef8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e8ef8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8ef8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8ef8-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8ef8-125">IID</span><span class="sxs-lookup"><span data-stu-id="e8ef8-125">IID</span></span><br/>                      | <span data-ttu-id="e8ef8-126">IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="e8ef8-126">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="e8ef8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8ef8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ef8-128">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="e8ef8-128">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





