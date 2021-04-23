---
title: IMsRdpDriveV2 Дривелеттериндекс, свойство
description: Содержит индекс буквы диска.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дривелеттериндекс
- Службы удаленных рабочих столов свойства Дривелеттериндекс, интерфейс IMsRdpDriveV2
- Службы удаленных рабочих столов интерфейса IMsRdpDriveV2, свойство Дривелеттериндекс
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989409"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a><span data-ttu-id="39b2d-106">IMsRdpDriveV2: свойство Ривелеттериндекс:D</span><span class="sxs-lookup"><span data-stu-id="39b2d-106">IMsRdpDriveV2::DriveLetterIndex property</span></span>

<span data-ttu-id="39b2d-107">Содержит индекс буквы диска.</span><span class="sxs-lookup"><span data-stu-id="39b2d-107">Contains the index of the letter for the drive.</span></span>

<span data-ttu-id="39b2d-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="39b2d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b2d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39b2d-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a><span data-ttu-id="39b2d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="39b2d-110">Property value</span></span>

<span data-ttu-id="39b2d-111">Индекс буквы для диска.</span><span class="sxs-lookup"><span data-stu-id="39b2d-111">The index of the letter for the drive.</span></span> <span data-ttu-id="39b2d-112">0 = "A", 1 = "B" и т. д.</span><span class="sxs-lookup"><span data-stu-id="39b2d-112">0 = "A", 1 = "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b2d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="39b2d-113">Requirements</span></span>



| <span data-ttu-id="39b2d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="39b2d-114">Requirement</span></span> | <span data-ttu-id="39b2d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="39b2d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39b2d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39b2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39b2d-117">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="39b2d-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="39b2d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39b2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39b2d-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39b2d-119">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="39b2d-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="39b2d-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="39b2d-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b2d-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="39b2d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="39b2d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39b2d-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b2d-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b2d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39b2d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b2d-125">**IMsRdpDriveV2**</span><span class="sxs-lookup"><span data-stu-id="39b2d-125">**IMsRdpDriveV2**</span></span>](imsrdpdrivev2.md)
</dt> </dl>

 

 





