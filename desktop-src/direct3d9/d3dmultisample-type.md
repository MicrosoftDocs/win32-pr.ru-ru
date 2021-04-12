---
description: Определяет уровни многофакторной множественной выборки, которую может применить устройство.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: Перечисление D3DMULTISAMPLE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: da8f9c1c8bb3aa74c0ab22a5cc701e7d835898de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355063"
---
# <a name="d3dmultisample_type-enumeration"></a><span data-ttu-id="8559a-103">\_Перечисление типов D3DMULTISAMPLE</span><span class="sxs-lookup"><span data-stu-id="8559a-103">D3DMULTISAMPLE\_TYPE enumeration</span></span>

<span data-ttu-id="8559a-104">Определяет уровни многофакторной множественной выборки, которую может применить устройство.</span><span class="sxs-lookup"><span data-stu-id="8559a-104">Defines the levels of full-scene multisampling that the device can apply.</span></span>

## <a name="syntax"></a><span data-ttu-id="8559a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8559a-105">Syntax</span></span>


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="8559a-106">Константы</span><span class="sxs-lookup"><span data-stu-id="8559a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8559a-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ None**</span><span class="sxs-lookup"><span data-stu-id="8559a-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-108">Уровень многоуровневой выборки в полноэкранном режиме недоступен.</span><span class="sxs-lookup"><span data-stu-id="8559a-108">No level of full-scene multisampling is available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE не \_ маскирует**</span><span class="sxs-lookup"><span data-stu-id="8559a-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE\_NONMASKABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="8559a-110">Включает значение свойства "многовыборочное качество".</span><span class="sxs-lookup"><span data-stu-id="8559a-110">Enables the multisample quality value.</span></span> <span data-ttu-id="8559a-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="8559a-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**\_Примеры D3DMULTISAMPLE 2 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE\_2\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-113">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-113">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**\_Примеры D3DMULTISAMPLE 3 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE\_3\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-115">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-115">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**\_Примеры D3DMULTISAMPLE 4 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE\_4\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-117">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-117">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**\_Примеры D3DMULTISAMPLE 5 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE\_5\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-119">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-119">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**\_Примеры D3DMULTISAMPLE 6 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE\_6\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-121">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-121">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**\_Примеры D3DMULTISAMPLE 7 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE\_7\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-123">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-123">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**\_Примеры D3DMULTISAMPLE 8 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE\_8\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-125">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-125">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**\_Примеры D3DMULTISAMPLE 9 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE\_9\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-127">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-127">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**\_Примеры D3DMULTISAMPLE 10 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE\_10\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-129">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-129">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**\_Примеры D3DMULTISAMPLE 11 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE\_11\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-131">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-131">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**\_Примеры D3DMULTISAMPLE 12 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE\_12\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-133">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-133">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**\_Примеры D3DMULTISAMPLE 13 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE\_13\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-135">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-135">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**\_Примеры D3DMULTISAMPLE 14 \_**</span><span class="sxs-lookup"><span data-stu-id="8559a-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE\_14\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-137">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-137">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE \_ 15 \_ примеров**</span><span class="sxs-lookup"><span data-stu-id="8559a-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE\_15\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-139">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-139">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE \_ 16 \_ примеров**</span><span class="sxs-lookup"><span data-stu-id="8559a-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE\_16\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-141">Уровень полноэкранного мультисэмплинга.</span><span class="sxs-lookup"><span data-stu-id="8559a-141">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8559a-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8559a-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8559a-143">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="8559a-143">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8559a-144">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="8559a-144">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8559a-145">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="8559a-145">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8559a-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8559a-146">Remarks</span></span>

<span data-ttu-id="8559a-147">Помимо включения многовыборочной множественной выборки в [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) , будут отображаться состояния отрисовки, которые включают и отключают различные аспекты на детализированном уровне.</span><span class="sxs-lookup"><span data-stu-id="8559a-147">In addition to enabling full-scene multisampling at [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, there will be render states that turn various aspects on and off at fine-grained levels.</span></span>

<span data-ttu-id="8559a-148">Множественная выборка допустима только для цепочки буферов, которая создается или сбрасывается с помощью D3DSWAPEFFECT \_ отмены переключения.</span><span class="sxs-lookup"><span data-stu-id="8559a-148">Multisampling is valid only on a swap chain that is being created or reset with the D3DSWAPEFFECT\_DISCARD swap effect.</span></span>

<span data-ttu-id="8559a-149">Значение многовыборочного сглаживания можно задать с помощью параметров (или подпараметров) в следующих методах.</span><span class="sxs-lookup"><span data-stu-id="8559a-149">The multisample antialiasing value can be set with the parameters (or sub-parameters) in the following methods.</span></span>



| <span data-ttu-id="8559a-150">Метод</span><span class="sxs-lookup"><span data-stu-id="8559a-150">Method</span></span>                                                                                             | <span data-ttu-id="8559a-151">Параметры</span><span class="sxs-lookup"><span data-stu-id="8559a-151">Parameters</span></span>                         | <span data-ttu-id="8559a-152">Подпараметры</span><span class="sxs-lookup"><span data-stu-id="8559a-152">Sub-parameters</span></span>                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [<span data-ttu-id="8559a-153">**IDirect3D9:: Чеккдевицемултисамплетипе**</span><span class="sxs-lookup"><span data-stu-id="8559a-153">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | <span data-ttu-id="8559a-154">Мултисамплетипе и Пкуалитилевелс</span><span class="sxs-lookup"><span data-stu-id="8559a-154">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="8559a-155">**IDirect3D9:: Креатедевице**</span><span class="sxs-lookup"><span data-stu-id="8559a-155">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | <span data-ttu-id="8559a-156">ппресентатионпараметерс</span><span class="sxs-lookup"><span data-stu-id="8559a-156">pPresentationParameters</span></span>            | <span data-ttu-id="8559a-157">Мултисамплетипе и Пкуалитилевелс</span><span class="sxs-lookup"><span data-stu-id="8559a-157">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="8559a-158">**IDirect3DDevice9:: Креатеаддитионалсвапчаин**</span><span class="sxs-lookup"><span data-stu-id="8559a-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | <span data-ttu-id="8559a-159">ппресентатионпараметерс</span><span class="sxs-lookup"><span data-stu-id="8559a-159">pPresentationParameters</span></span>            | <span data-ttu-id="8559a-160">Мултисамплетипе и Пкуалитилевелс</span><span class="sxs-lookup"><span data-stu-id="8559a-160">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="8559a-161">**IDirect3DDevice9:: КреатедепсстенЦилсурфаце**</span><span class="sxs-lookup"><span data-stu-id="8559a-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | <span data-ttu-id="8559a-162">Мултисамплетипе и Пкуалитилевелс</span><span class="sxs-lookup"><span data-stu-id="8559a-162">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="8559a-163">**IDirect3DDevice9:: Креатерендертаржет**</span><span class="sxs-lookup"><span data-stu-id="8559a-163">**IDirect3DDevice9::CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | <span data-ttu-id="8559a-164">Мултисамплетипе и Пкуалитилевелс</span><span class="sxs-lookup"><span data-stu-id="8559a-164">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="8559a-165">**IDirect3DDevice9::Reset**</span><span class="sxs-lookup"><span data-stu-id="8559a-165">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | <span data-ttu-id="8559a-166">ппресентатионпараметерс</span><span class="sxs-lookup"><span data-stu-id="8559a-166">pPresentationParameters</span></span>            | <span data-ttu-id="8559a-167">Мултисамплетипе и Пкуалитилевелс</span><span class="sxs-lookup"><span data-stu-id="8559a-167">MultiSampleType and pQualityLevels</span></span> |



 

<span data-ttu-id="8559a-168">Не рекомендуется переключаться с одного многопримерного типа на другой, чтобы повысить качество сглаживания.</span><span class="sxs-lookup"><span data-stu-id="8559a-168">It is not good practice to switch from one multisample type to another to raise the quality of the antialiasing.</span></span>

<span data-ttu-id="8559a-169">D3DMULTISAMPLE \_ None включает эффекты переключения, отличные от отмены, блокировки и т. д.</span><span class="sxs-lookup"><span data-stu-id="8559a-169">D3DMULTISAMPLE\_NONE enables swap effects other than discarding, locking, and so on.</span></span>

<span data-ttu-id="8559a-170">Поддерживает ли устройство с маской многофакторную выборку (более одного образца для формата с несколькими образцами, а также поддержка сглаживания) или только немаскированная многовыборка (поддержка сглаживания), драйвер устройства предоставляет количество уровней качества для D3DMULTISAMPLE \_ НЕмаскированных многопримерных типов.</span><span class="sxs-lookup"><span data-stu-id="8559a-170">Whether the display device supports maskable multisampling (more than one sample for a multiple-sample render-target format plus antialias support) or just non-maskable multisampling (only antialias support), the driver for the device provides the number of quality levels for the D3DMULTISAMPLE\_NONMASKABLE multiple-sample type.</span></span> <span data-ttu-id="8559a-171">Приложения, которые просто используют многовыборочную поддержку для сглаживания, должны запрашивать только число уровней качества, поддерживаемых драйвером.</span><span class="sxs-lookup"><span data-stu-id="8559a-171">Applications that just use multisampling for antialiasing purposes only need to query for the number of non-maskable multiple-sample quality levels that the driver supports.</span></span>

<span data-ttu-id="8559a-172">Уровни качества, поддерживаемые устройством, можно получить с помощью параметра Пкуалитилевелс [**IDirect3D9:: чеккдевицемултисамплетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="8559a-172">The quality levels supported by the device can be obtained with the pQualityLevels parameter of [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="8559a-173">Уровни качества, используемые приложением, задаются с помощью параметра Мултисамплекуалити [**IDirect3DDevice9:: креатедепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) и [**IDirect3DDevice9:: креатерендертаржет**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span><span class="sxs-lookup"><span data-stu-id="8559a-173">Quality levels used by the application are set with the MultiSampleQuality parameter of [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) and [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span></span>

<span data-ttu-id="8559a-174">\_Описание многовыборочной множественной выборки см. в разделе D3DRS мултисамплемаск.</span><span class="sxs-lookup"><span data-stu-id="8559a-174">See D3DRS\_MULTISAMPLEMASK for discussion of maskable multisampling.</span></span>

## <a name="requirements"></a><span data-ttu-id="8559a-175">Требования</span><span class="sxs-lookup"><span data-stu-id="8559a-175">Requirements</span></span>



| <span data-ttu-id="8559a-176">Требование</span><span class="sxs-lookup"><span data-stu-id="8559a-176">Requirement</span></span> | <span data-ttu-id="8559a-177">Значение</span><span class="sxs-lookup"><span data-stu-id="8559a-177">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8559a-178">Header</span><span class="sxs-lookup"><span data-stu-id="8559a-178">Header</span></span><br/> | <dl> <span data-ttu-id="8559a-179"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8559a-179"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8559a-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8559a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8559a-181">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="8559a-181">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8559a-182">**\_Параметры D3DPRESENT**</span><span class="sxs-lookup"><span data-stu-id="8559a-182">**D3DPRESENT\_PARAMETERS**</span></span>](d3dpresent-parameters.md)
</dt> <dt>

[<span data-ttu-id="8559a-183">**D3DSURFACE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8559a-183">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> </dl>

 

 
