---
description: Указывает окно для механизма мультимедиа, применяемого для защиты выходных данных Protection Manager (ОПМ).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Атрибут MF_MEDIA_ENGINE_OPM_HWND (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999889"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a><span data-ttu-id="7c99e-103">\_ \_ \_ Атрибут HWND ОПМ обработчика передачи мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="7c99e-103">MF\_MEDIA\_ENGINE\_OPM\_HWND attribute</span></span>

<span data-ttu-id="7c99e-104">Указывает окно для механизма мультимедиа, применяемого для защиты [выходных данных Protection Manager](output-protection-manager.md) (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="7c99e-104">Specifies a window for the Media Engine to apply [Output Protection Manager](output-protection-manager.md) (OPM) protections.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c99e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7c99e-105">Data type</span></span>

<span data-ttu-id="7c99e-106">**HWND** хранится как **UINT64**</span><span class="sxs-lookup"><span data-stu-id="7c99e-106">**HWND** stored as **UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="7c99e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c99e-107">Remarks</span></span>

<span data-ttu-id="7c99e-108">Этот атрибут используется с методом [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) для инициализации механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7c99e-108">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="7c99e-109">Чтобы включить защиту ОПМ для воспроизведения видео, приложение должно выполнить одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="7c99e-109">To enable OPM protections for video playback, the application must do one of the following:</span></span>

-   <span data-ttu-id="7c99e-110">При создании подсистемы мультимедиа задайте атрибут [ \_ \_ \_ \_ HWND для воспроизведения обработчика мультимедиа MF](mf-media-engine-playback-hwnd.md) .</span><span class="sxs-lookup"><span data-stu-id="7c99e-110">Set the [MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND](mf-media-engine-playback-hwnd.md) attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="7c99e-111">Задайте \_ \_ атрибут HWND ОПМ Engine для обработчика мультимедиа \_ \_ при создании подсистемы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7c99e-111">Set the MF\_MEDIA\_ENGINE\_OPM\_HWND attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="7c99e-112">Вызовите [**имфмедиаенгинепротектедконтент:: сетопмвиндов**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) в любой точке после создания обработчика мультимедиа, но до отображения защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="7c99e-112">Call [**IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) at any point after creating the Media Engine, but before protected content is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c99e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7c99e-113">Requirements</span></span>



| <span data-ttu-id="7c99e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7c99e-114">Requirement</span></span> | <span data-ttu-id="7c99e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7c99e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c99e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c99e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c99e-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c99e-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="7c99e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c99e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c99e-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c99e-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="7c99e-120">Header</span><span class="sxs-lookup"><span data-stu-id="7c99e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c99e-121"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c99e-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c99e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c99e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c99e-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c99e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c99e-124">Атрибуты обработчика мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7c99e-124">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> </dl>

 

 




