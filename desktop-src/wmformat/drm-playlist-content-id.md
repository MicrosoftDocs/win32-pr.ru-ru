---
title: Структура DRM_PLAYLIST_CONTENT_ID (Дрмекстерналс. h)
description: '\_ \_ Структура идентификатора содержимого списка воспроизведения DRM \_ содержит сведения о содержимом, которое должно быть скопировано на компакт-диск в процессе записи списка воспроизведения.'
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- Формат DRM_PLAYLIST_CONTENT_ID структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701066"
---
# <a name="drm_playlist_content_id-structure"></a><span data-ttu-id="831fd-105">\_ \_ Структура идентификатора содержимого списка воспроизведения DRM \_</span><span class="sxs-lookup"><span data-stu-id="831fd-105">DRM\_PLAYLIST\_CONTENT\_ID structure</span></span>

<span data-ttu-id="831fd-106">Структура **\_ \_ \_ идентификатора содержимого списка воспроизведения DRM** содержит сведения о содержимом, которое должно быть скопировано на компакт-диск в процессе записи списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="831fd-106">The **DRM\_PLAYLIST\_CONTENT\_ID** structure contains information about content that is to be copied to CD as part of a playlist burn.</span></span>

## <a name="syntax"></a><span data-ttu-id="831fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="831fd-107">Syntax</span></span>


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a><span data-ttu-id="831fd-108">Члены</span><span class="sxs-lookup"><span data-stu-id="831fd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="831fd-109">**lpcwszV2Header**</span><span class="sxs-lookup"><span data-stu-id="831fd-109">**lpcwszV2Header**</span></span>
</dt> <dd>

<span data-ttu-id="831fd-110">Заголовок DRM.</span><span class="sxs-lookup"><span data-stu-id="831fd-110">DRM header.</span></span> <span data-ttu-id="831fd-111">Используйте этот элемент, если содержимое защищено с помощью Windows Media DRM версии 2 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="831fd-111">Use this member if the content is protected by Windows Media DRM version 2 or later.</span></span>

</dd> <dt>

<span data-ttu-id="831fd-112">**lpcszV1KID**</span><span class="sxs-lookup"><span data-stu-id="831fd-112">**lpcszV1KID**</span></span>
</dt> <dd>

<span data-ttu-id="831fd-113">идентификатор ключа;</span><span class="sxs-lookup"><span data-stu-id="831fd-113">Key ID.</span></span> <span data-ttu-id="831fd-114">Используйте этот элемент, если содержимое защищено с помощью Windows Media DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="831fd-114">Use this member if the content is protected by Windows Media DRM version 1.</span></span>

</dd> <dt>

<span data-ttu-id="831fd-115">**пбосердата**</span><span class="sxs-lookup"><span data-stu-id="831fd-115">**pbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="831fd-116">Буфер, содержащий дополнительные данные.</span><span class="sxs-lookup"><span data-stu-id="831fd-116">Buffer containing supplementary data.</span></span>

</dd> <dt>

<span data-ttu-id="831fd-117">**кбосердата**</span><span class="sxs-lookup"><span data-stu-id="831fd-117">**cbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="831fd-118">Размер буфера **пбосердата** в байтах.</span><span class="sxs-lookup"><span data-stu-id="831fd-118">Size of the **pbOtherData** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="831fd-119">**двуникуеидфорсессион**</span><span class="sxs-lookup"><span data-stu-id="831fd-119">**dwUniqueIDForSession**</span></span>
</dt> <dd>

<span data-ttu-id="831fd-120">Уникальный идентификатор содержимого, которое будет использоваться в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="831fd-120">Unique identifier for the content to be used in the current session.</span></span>

</dd> <dt>

<span data-ttu-id="831fd-121">**дввалидфиелдс**</span><span class="sxs-lookup"><span data-stu-id="831fd-121">**dwValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="831fd-122">**DWORD** , указывающий допустимые поля этой структуры.</span><span class="sxs-lookup"><span data-stu-id="831fd-122">**DWORD** indicating the valid fields of this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="831fd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="831fd-123">Requirements</span></span>



| <span data-ttu-id="831fd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="831fd-124">Requirement</span></span> | <span data-ttu-id="831fd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="831fd-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="831fd-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="831fd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="831fd-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="831fd-127">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="831fd-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="831fd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="831fd-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="831fd-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="831fd-130">Версия</span><span class="sxs-lookup"><span data-stu-id="831fd-130">Version</span></span><br/>                  | <span data-ttu-id="831fd-131">Пакет SDK для Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="831fd-131">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="831fd-132">Header</span><span class="sxs-lookup"><span data-stu-id="831fd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="831fd-133"><dt>Дрмекстерналс. h</dt></span><span class="sxs-lookup"><span data-stu-id="831fd-133"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="831fd-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="831fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831fd-135">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="831fd-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





