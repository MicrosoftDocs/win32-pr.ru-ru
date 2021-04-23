---
title: IMsRdpClientAdvancedSettings7 Видеоплайбаккмоде, свойство
description: Указывает или получает значение, указывающее режим воспроизведения видео.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Видеоплайбаккмоде
- Службы удаленных рабочих столов свойства Видеоплайбаккмоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Видеоплайбаккмоде
- Службы удаленных рабочих столов свойства Видеоплайбаккмоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Видеоплайбаккмоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416161"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a><span data-ttu-id="451c1-108">Свойство IMsRdpClientAdvancedSettings7:: Видеоплайбаккмоде</span><span class="sxs-lookup"><span data-stu-id="451c1-108">IMsRdpClientAdvancedSettings7::VideoPlaybackMode property</span></span>

<span data-ttu-id="451c1-109">Указывает или получает значение, указывающее режим воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="451c1-109">Specifies or retrieves a value that indicates the video playback mode.</span></span>

<span data-ttu-id="451c1-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="451c1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="451c1-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="451c1-111">Syntax</span></span>


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a><span data-ttu-id="451c1-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="451c1-112">Property value</span></span>

<span data-ttu-id="451c1-113">Значение, указывающее режим воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="451c1-113">A value that specifies the video playback mode.</span></span>

<span data-ttu-id="451c1-114">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="451c1-114">The possible values are:</span></span>

<dt>

<span data-ttu-id="451c1-115">1</span><span class="sxs-lookup"><span data-stu-id="451c1-115">1</span></span>
</dt> <dd>

<span data-ttu-id="451c1-116">Режим воспроизведения видео по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="451c1-116">The default video playback mode.</span></span> <span data-ttu-id="451c1-117">Если для режима воспроизведения видео задано это значение, перенаправление видео управляется свойством [**аудиоредиректионмоде**](imsrdpclientsecuredsettings-autoredirectionmode.md) .</span><span class="sxs-lookup"><span data-stu-id="451c1-117">When the video playback mode is set to this value, video redirection is controlled by the [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) property.</span></span> <span data-ttu-id="451c1-118">Если для свойства **аудиоредиректионмоде** задано **\_ \_ перенаправление в звуковом режиме**, видео декодировано и отображается на клиенте.</span><span class="sxs-lookup"><span data-stu-id="451c1-118">When the **AudioRedirectionMode** property is set to **AUDIO\_MODE\_REDIRECT**, video is decoded and rendered on the client.</span></span>

</dd> <dt>

<span data-ttu-id="451c1-119">0</span><span class="sxs-lookup"><span data-stu-id="451c1-119">0</span></span>
</dt> <dd>

<span data-ttu-id="451c1-120">Перенаправление воспроизведения видео отключено, даже если для [**аудиоредиректионмоде**](imsrdpclientsecuredsettings-autoredirectionmode.md) задано **\_ \_ перенаправление в звуковом режиме**.</span><span class="sxs-lookup"><span data-stu-id="451c1-120">Video playback redirection is disabled, even when [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) is set to **AUDIO\_MODE\_REDIRECT**.</span></span> <span data-ttu-id="451c1-121">В этом режиме видео декодировано и отображается на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="451c1-121">In this mode, video is decoded and rendered on the RD Session Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="451c1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="451c1-122">Requirements</span></span>



| <span data-ttu-id="451c1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="451c1-123">Requirement</span></span> | <span data-ttu-id="451c1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="451c1-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="451c1-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="451c1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="451c1-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="451c1-126">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="451c1-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="451c1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="451c1-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="451c1-128">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="451c1-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="451c1-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="451c1-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="451c1-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="451c1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="451c1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="451c1-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="451c1-132"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="451c1-133">IID</span><span class="sxs-lookup"><span data-stu-id="451c1-133">IID</span></span><br/>                      | <span data-ttu-id="451c1-134">IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="451c1-134">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="451c1-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="451c1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451c1-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="451c1-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="451c1-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="451c1-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





