---
title: IMsRdpClientAdvancedSettings7 Аудиокуалитимоде, свойство
description: Указывает или получает значение, указывающее параметр режима качества звука для перенаправленного звука. По умолчанию установлено значение 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аудиокуалитимоде
- Службы удаленных рабочих столов свойства Аудиокуалитимоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Аудиокуалитимоде
- Службы удаленных рабочих столов свойства Аудиокуалитимоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Аудиокуалитимоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681938"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a><span data-ttu-id="e6c1b-109">Свойство IMsRdpClientAdvancedSettings7:: Аудиокуалитимоде</span><span class="sxs-lookup"><span data-stu-id="e6c1b-109">IMsRdpClientAdvancedSettings7::AudioQualityMode property</span></span>

<span data-ttu-id="e6c1b-110">Указывает или получает значение, указывающее параметр режима качества звука для перенаправленного звука.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-110">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span> <span data-ttu-id="e6c1b-111">По умолчанию установлено значение 0.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-111">By default this is set to 0.</span></span>

<span data-ttu-id="e6c1b-112">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c1b-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6c1b-113">Syntax</span></span>


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a><span data-ttu-id="e6c1b-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e6c1b-114">Property value</span></span>

<span data-ttu-id="e6c1b-115">Значение типа, указывающее режим качества звука.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-115">A value that specifies the audio quality mode.</span></span>

<span data-ttu-id="e6c1b-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e6c1b-116">The possible values are:</span></span>

<dt>

<span data-ttu-id="e6c1b-117">0</span><span class="sxs-lookup"><span data-stu-id="e6c1b-117">0</span></span>
</dt> <dd>

<span data-ttu-id="e6c1b-118">Динамическое качество звука.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-118">Dynamic audio quality.</span></span> <span data-ttu-id="e6c1b-119">Это параметр качества звука по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-119">This is the default audio quality setting.</span></span> <span data-ttu-id="e6c1b-120">Сервер динамически корректирует качество вывода звука в ответ на условия сети и возможности клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-120">The server dynamically adjusts audio output quality in response to network conditions and the client and server capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="e6c1b-121">1</span><span class="sxs-lookup"><span data-stu-id="e6c1b-121">1</span></span>
</dt> <dd>

<span data-ttu-id="e6c1b-122">Средний качество звука.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-122">Medium audio quality.</span></span> <span data-ttu-id="e6c1b-123">Сервер использует фиксированный, но сжатый формат для вывода звука.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-123">The server uses a fixed but compressed format for audio output.</span></span>

</dd> <dt>

<span data-ttu-id="e6c1b-124">2</span><span class="sxs-lookup"><span data-stu-id="e6c1b-124">2</span></span>
</dt> <dd>

<span data-ttu-id="e6c1b-125">Высокое качество звука.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-125">High audio quality.</span></span> <span data-ttu-id="e6c1b-126">Сервер предоставляет выходные данные в несжатом формате PCM с меньшими затратами на обработку для задержки.</span><span class="sxs-lookup"><span data-stu-id="e6c1b-126">The server provides audio output in uncompressed PCM format with lower processing overhead for latency.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6c1b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e6c1b-127">Requirements</span></span>



| <span data-ttu-id="e6c1b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e6c1b-128">Requirement</span></span> | <span data-ttu-id="e6c1b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e6c1b-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c1b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6c1b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c1b-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6c1b-131">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="e6c1b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6c1b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c1b-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6c1b-133">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="e6c1b-134">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e6c1b-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6c1b-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c1b-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e6c1b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c1b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6c1b-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c1b-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e6c1b-138">IID</span><span class="sxs-lookup"><span data-stu-id="e6c1b-138">IID</span></span><br/>                      | <span data-ttu-id="e6c1b-139">IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="e6c1b-139">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6c1b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6c1b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c1b-141">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e6c1b-141">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e6c1b-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e6c1b-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





