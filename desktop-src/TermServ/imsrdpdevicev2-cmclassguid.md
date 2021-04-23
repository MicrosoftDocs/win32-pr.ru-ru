---
title: IMsRdpDeviceV2 Кмклассгуид, свойство
description: Содержит GUID класса установки Configuration Manager для устройства.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Кмклассгуид
- Службы удаленных рабочих столов свойства Кмклассгуид, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Кмклассгуид
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672463"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a><span data-ttu-id="33a44-106">Свойство IMsRdpDeviceV2:: Кмклассгуид</span><span class="sxs-lookup"><span data-stu-id="33a44-106">IMsRdpDeviceV2::CmClassGuid property</span></span>

<span data-ttu-id="33a44-107">Содержит GUID класса установки Configuration Manager для устройства.</span><span class="sxs-lookup"><span data-stu-id="33a44-107">Contains the configuration manager setup class GUID for the device.</span></span>

<span data-ttu-id="33a44-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="33a44-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a44-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33a44-109">Syntax</span></span>


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a><span data-ttu-id="33a44-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="33a44-110">Property value</span></span>

<span data-ttu-id="33a44-111">Идентификатор GUID класса установки Configuration Manager для устройства.</span><span class="sxs-lookup"><span data-stu-id="33a44-111">The configuration manager setup class GUID for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a44-112">Требования</span><span class="sxs-lookup"><span data-stu-id="33a44-112">Requirements</span></span>



| <span data-ttu-id="33a44-113">Требование</span><span class="sxs-lookup"><span data-stu-id="33a44-113">Requirement</span></span> | <span data-ttu-id="33a44-114">Значение</span><span class="sxs-lookup"><span data-stu-id="33a44-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33a44-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33a44-115">Minimum supported client</span></span><br/> | <span data-ttu-id="33a44-116">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="33a44-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="33a44-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33a44-117">Minimum supported server</span></span><br/> | <span data-ttu-id="33a44-118">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="33a44-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="33a44-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="33a44-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="33a44-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33a44-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="33a44-121">DLL</span><span class="sxs-lookup"><span data-stu-id="33a44-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33a44-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33a44-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="33a44-123">IID</span><span class="sxs-lookup"><span data-stu-id="33a44-123">IID</span></span><br/>                      | <span data-ttu-id="33a44-124">IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="33a44-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="33a44-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33a44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a44-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="33a44-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





