---
title: IMsRdpClientAdvancedSettings5 Аудиоредиректионмоде, свойство
description: Задает и получает режим перенаправления звука и различные параметры перенаправления звука.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Аудиоредиректионмоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40be8b8e63f210d060c0f585c9fe31328ac6ed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340525"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a><span data-ttu-id="dd7a3-112">Свойство IMsRdpClientAdvancedSettings5:: Аудиоредиректионмоде</span><span class="sxs-lookup"><span data-stu-id="dd7a3-112">IMsRdpClientAdvancedSettings5::AudioRedirectionMode property</span></span>

<span data-ttu-id="dd7a3-113">Задает и получает режим перенаправления звука и различные параметры перенаправления звука.</span><span class="sxs-lookup"><span data-stu-id="dd7a3-113">Sets and retrieves the audio redirection mode and different audio redirection options.</span></span>

<span data-ttu-id="dd7a3-114">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="dd7a3-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd7a3-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd7a3-115">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="dd7a3-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dd7a3-116">Property value</span></span>

<span data-ttu-id="dd7a3-117">Задает различные значения для режима перенаправления звука.</span><span class="sxs-lookup"><span data-stu-id="dd7a3-117">Sets different values for the audio redirection mode.</span></span> <span data-ttu-id="dd7a3-118">Этот параметр имеет следующие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="dd7a3-118">This parameter has the following possible values.</span></span>

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

<span data-ttu-id="dd7a3-119">**Звуковые \_ файлы РЕЖИМ \_ перенаправления 0** (перенаправление звука включено, а параметр перенаправления — "перенаправление на этот компьютер").</span><span class="sxs-lookup"><span data-stu-id="dd7a3-119">**AUDIO\_MODE\_REDIRECT 0** (Audio redirection is enabled and the option for redirection is "Bring to this computer".</span></span> <span data-ttu-id="dd7a3-120">Это режим по умолчанию.)</span><span class="sxs-lookup"><span data-stu-id="dd7a3-120">This is the default mode.)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

<span data-ttu-id="dd7a3-121">**Звуковые \_ файлы РЕЖИМ \_ воспроизведения \_ на \_ сервере 1** (включено перенаправление звука, а параметр — "оставить на удаленном компьютере").</span><span class="sxs-lookup"><span data-stu-id="dd7a3-121">**AUDIO\_MODE\_PLAY\_ON\_SERVER 1** (Audio redirection is enabled and the option is "Leave at remote computer".</span></span> <span data-ttu-id="dd7a3-122">Параметр "оставить на удаленном компьютере" поддерживается только при удаленном подключении к главному компьютеру под управлением Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd7a3-122">The "Leave at remote computer" option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="dd7a3-123">Если подключение установлено к главному компьютеру под Windows Server 2008, параметр "оставить на удаленном компьютере" изменится на "не воспроизводить".)</span><span class="sxs-lookup"><span data-stu-id="dd7a3-123">If the connection is to a host computer that is running Windows Server 2008, the option "Leave at remote computer" is changed to "Do not play".)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

<span data-ttu-id="dd7a3-124">**Звуковые \_ файлы РЕЖИМ \_ нет 2** (перенаправление звука включено, а режим — "не воспроизводить").</span><span class="sxs-lookup"><span data-stu-id="dd7a3-124">**AUDIO\_MODE\_NONE 2** (Audio redirection is enabled and the mode is "Do not play".)</span></span>


<span data-ttu-id="dd7a3-125"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dd7a3-125"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dd7a3-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dd7a3-126">Requirements</span></span>



| <span data-ttu-id="dd7a3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dd7a3-127">Requirement</span></span> | <span data-ttu-id="dd7a3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dd7a3-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd7a3-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd7a3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd7a3-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd7a3-130">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="dd7a3-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd7a3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd7a3-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd7a3-132">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="dd7a3-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dd7a3-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd7a3-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd7a3-134"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="dd7a3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dd7a3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd7a3-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd7a3-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="dd7a3-137">IID</span><span class="sxs-lookup"><span data-stu-id="dd7a3-137">IID</span></span><br/>                      | <span data-ttu-id="dd7a3-138">IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="dd7a3-138">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd7a3-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd7a3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd7a3-140">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="dd7a3-140">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="dd7a3-141">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="dd7a3-141">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="dd7a3-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="dd7a3-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="dd7a3-143">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="dd7a3-143">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





