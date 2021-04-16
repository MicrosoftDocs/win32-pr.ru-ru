---
title: Перечисление Клиентспек
description: Используется со свойством Клиентпротоколспек для указания протокола удаленного рабочего стола, используемого между клиентом и сервером.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Клиентспек
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672520"
---
# <a name="clientspec-enumeration"></a><span data-ttu-id="484fd-104">Перечисление Клиентспек</span><span class="sxs-lookup"><span data-stu-id="484fd-104">ClientSpec enumeration</span></span>

<span data-ttu-id="484fd-105">Используется со свойством [**клиентпротоколспек**](imsrdpclientadvancedsettings8-clientprotocolspec.md) для указания протокола удаленного рабочего стола, используемого между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="484fd-105">Used with the [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) property to specify the remote desktop protocol used between the client and the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="484fd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="484fd-106">Syntax</span></span>


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a><span data-ttu-id="484fd-107">Константы</span><span class="sxs-lookup"><span data-stu-id="484fd-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="484fd-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**фуллмоде**</span><span class="sxs-lookup"><span data-stu-id="484fd-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span></span>
</dt> <dd>

<span data-ttu-id="484fd-109">Это полный протокол удаленный рабочий стол Windows 8.</span><span class="sxs-lookup"><span data-stu-id="484fd-109">The protocol is full Windows 8 Remote Desktop protocol.</span></span>

</dd> <dt>

<span data-ttu-id="484fd-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**синклиентмоде**</span><span class="sxs-lookup"><span data-stu-id="484fd-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span></span>
</dt> <dd>

<span data-ttu-id="484fd-111">Протокол ограничен использованием кодеков RemoteFX для Windows 7 с пакетом обновления 1 (SP1) и более компактного кэша.</span><span class="sxs-lookup"><span data-stu-id="484fd-111">The protocol is limited to using the Windows 7 with SP1 RemoteFX codec and a smaller cache.</span></span> <span data-ttu-id="484fd-112">Все остальные кодеки отключены.</span><span class="sxs-lookup"><span data-stu-id="484fd-112">All other codecs are disabled.</span></span> <span data-ttu-id="484fd-113">Этот протокол имеет наименьший объем памяти.</span><span class="sxs-lookup"><span data-stu-id="484fd-113">This protocol has the smallest memory footprint.</span></span>

</dd> <dt>

<span data-ttu-id="484fd-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**смаллкачемоде**</span><span class="sxs-lookup"><span data-stu-id="484fd-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span></span>
</dt> <dd>

<span data-ttu-id="484fd-115">Протокол аналогичен **фуллмоде**, за исключением того, что он использует меньший кэш.</span><span class="sxs-lookup"><span data-stu-id="484fd-115">The protocol is the same as **FullMode**, except it uses a smaller cache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="484fd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="484fd-116">Requirements</span></span>



| <span data-ttu-id="484fd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="484fd-117">Requirement</span></span> | <span data-ttu-id="484fd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="484fd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="484fd-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="484fd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="484fd-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="484fd-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="484fd-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="484fd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="484fd-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="484fd-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="484fd-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="484fd-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="484fd-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="484fd-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="484fd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="484fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="484fd-126">**IMsRdpClientAdvancedSettings8:: Клиентпротоколспек**</span><span class="sxs-lookup"><span data-stu-id="484fd-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span></span>](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





