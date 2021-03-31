---
title: Перечисление DownloadMode (Deliveryoptimization. h)
description: Определяет различные режимы загрузки, используемые оптимизацией доставки.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- Использование BITS в обход оптимизации доставки. Используйте этот режим, например, чтобы клиенты могли использовать BranchCache. перечисление
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071542"
---
# <a name="downloadmode-enumeration"></a><span data-ttu-id="da402-106">Перечисление DownloadMode</span><span class="sxs-lookup"><span data-stu-id="da402-106">DownloadMode enumeration</span></span>

<span data-ttu-id="da402-107">Определяет различные режимы загрузки, используемые оптимизацией доставки.</span><span class="sxs-lookup"><span data-stu-id="da402-107">Defines the different download modes that Delivery Optimization uses.</span></span>

## <a name="syntax"></a><span data-ttu-id="da402-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da402-108">Syntax</span></span>


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a><span data-ttu-id="da402-109">Константы</span><span class="sxs-lookup"><span data-stu-id="da402-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da402-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span><span class="sxs-lookup"><span data-stu-id="da402-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span></span>
</dt> <dd>

<span data-ttu-id="da402-111">Этот параметр отключает одноранговый кэш, но по-прежнему позволяет оптимизировать доставку для загрузки содержимого с серверов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="da402-111">This setting disables peer-to-peer caching but still allows Delivery Optimization to download content from Microsoft servers.</span></span> <span data-ttu-id="da402-112">Этот режим использует дополнительные метаданные, предоставляемые облачными службами оптимизации доставки, для надежного и эффективного скачивания без одноранговых устройств.</span><span class="sxs-lookup"><span data-stu-id="da402-112">This mode uses additional metadata provided by the Delivery Optimization cloud services for a peerless reliable and efficient download experience.</span></span>

</dd> <dt>

<span data-ttu-id="da402-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span><span class="sxs-lookup"><span data-stu-id="da402-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span></span>
</dt> <dd>

<span data-ttu-id="da402-114">Это стандартный рабочий режим оптимизации доставки, обеспечивающий одноранговый обмен данными в пределах одной сети.</span><span class="sxs-lookup"><span data-stu-id="da402-114">This default operating mode for Delivery Optimization enables peer sharing on the same network.</span></span>

</dd> <dt>

<span data-ttu-id="da402-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span><span class="sxs-lookup"><span data-stu-id="da402-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span></span>
</dt> <dd>

<span data-ttu-id="da402-116">Если задан режим группы, Группа выбирается автоматически на основе сайта Device домен Active Directory Services (AD DS) (Windows 10, версия 1607) или домена, на который проверяется подлинность устройства (Windows 10, версия 1511).</span><span class="sxs-lookup"><span data-stu-id="da402-116">When group mode is set, the group is automatically selected based on the device s Active Directory Domain Services (AD DS) site (Windows 10, version 1607) or the domain the device is authenticated to (Windows 10, version 1511).</span></span> <span data-ttu-id="da402-117">В групповом режиме пиринг осуществляется по внутренним подсетям между устройствами, принадлежащим к одной и той же группе, включая устройства в удаленных офисах.</span><span class="sxs-lookup"><span data-stu-id="da402-117">In group mode, peering occurs across internal subnets, between devices that belong to the same group, including devices in remote offices.</span></span> <span data-ttu-id="da402-118">Вы можете использовать параметр GroupID для создания собственной пользовательской группы независимо от доменов и сайтов AD DS.</span><span class="sxs-lookup"><span data-stu-id="da402-118">You can use the GroupID option to create your own custom group independently of domains and AD DS sites.</span></span> <span data-ttu-id="da402-119">Режим групповой загрузки рекомендуется для большинства организаций, которые заинтересованы в оптимизации пропускной способности при оптимизации доставки.</span><span class="sxs-lookup"><span data-stu-id="da402-119">Group download mode is the recommended option for most organizations looking to achieve the best bandwidth optimization with Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="da402-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span><span class="sxs-lookup"><span data-stu-id="da402-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span></span>
</dt> <dd>

<span data-ttu-id="da402-121">Включение одноранговых интернет-источников для оптимизации доставки.</span><span class="sxs-lookup"><span data-stu-id="da402-121">Enable Internet peer sources for Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="da402-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span><span class="sxs-lookup"><span data-stu-id="da402-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span></span>
</dt> <dd>

<span data-ttu-id="da402-123">Простой режим полностью отключает использование облачных служб оптимизации доставки (для автономных сред).</span><span class="sxs-lookup"><span data-stu-id="da402-123">Simple mode disables the use of Delivery Optimization cloud services completely (for offline environments).</span></span> <span data-ttu-id="da402-124">Оптимизация доставки автоматически переходит в этот режим, если облачные службы оптимизации доставки недоступны, недостижимы или когда размер файла содержимого меньше 10 МБ.</span><span class="sxs-lookup"><span data-stu-id="da402-124">Delivery Optimization switches to this mode automatically when the Delivery Optimization cloud services are unavailable, unreachable or when the content file size is less than 10 MB.</span></span> <span data-ttu-id="da402-125">В этом режиме оптимизация доставки обеспечивает надежное скачивание без для однорангового кэширования.</span><span class="sxs-lookup"><span data-stu-id="da402-125">In this mode, Delivery Optimization provides a reliable download experience, with no peer-to-peer caching.</span></span>

</dd> <dt>

<span data-ttu-id="da402-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span><span class="sxs-lookup"><span data-stu-id="da402-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span></span>
</dt> <dd>

<span data-ttu-id="da402-127">Использование BITS в обход оптимизации доставки.</span><span class="sxs-lookup"><span data-stu-id="da402-127">Bypass Delivery Optimization and use BITS, instead.</span></span> <span data-ttu-id="da402-128">Используйте этот режим, например, чтобы клиенты могли использовать BranchCache.</span><span class="sxs-lookup"><span data-stu-id="da402-128">For example, select this mode so that clients can use BranchCache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da402-129">Требования</span><span class="sxs-lookup"><span data-stu-id="da402-129">Requirements</span></span>

| <span data-ttu-id="da402-130">Требование</span><span class="sxs-lookup"><span data-stu-id="da402-130">Requirement</span></span> | <span data-ttu-id="da402-131">Значение</span><span class="sxs-lookup"><span data-stu-id="da402-131">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="da402-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da402-132">Minimum supported client</span></span><br/> | <span data-ttu-id="da402-133">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="da402-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="da402-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da402-134">Minimum supported server</span></span><br/> | <span data-ttu-id="da402-135">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="da402-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="da402-136">Header</span><span class="sxs-lookup"><span data-stu-id="da402-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="da402-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="da402-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
