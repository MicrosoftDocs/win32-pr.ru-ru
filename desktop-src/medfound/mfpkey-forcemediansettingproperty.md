---
description: Указывает, должен ли кодек использовать медианную фильтрацию во время кодирования.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: Свойство MFPKEY_FORCEMEDIANSETTING (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914172"
---
# <a name="mfpkey_forcemediansetting-property"></a><span data-ttu-id="a2321-103">МФПКЭЙ \_ форцемедиансеттинг, свойство</span><span class="sxs-lookup"><span data-stu-id="a2321-103">MFPKEY\_FORCEMEDIANSETTING Property</span></span>

<span data-ttu-id="a2321-104">Указывает, должен ли кодек использовать медианную фильтрацию во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="a2321-104">Specifies whether the codec should use median filtering during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a2321-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="a2321-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a2321-106">g \_ всзвмвкфорцемедиансеттинг</span><span class="sxs-lookup"><span data-stu-id="a2321-106">g\_wszWMVCForceMedianSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="a2321-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a2321-107">Data Type</span></span>

<span data-ttu-id="a2321-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="a2321-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="a2321-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a2321-109">Default Value</span></span>

<span data-ttu-id="a2321-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="a2321-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="a2321-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2321-111">Remarks</span></span>

<span data-ttu-id="a2321-112">Функция медианы указывает, что кодек игнорирует шум и зернистость при вычислении движения между кадрами.</span><span class="sxs-lookup"><span data-stu-id="a2321-112">Median filtering tells the codec to ignore noise and grain when calculating motion between frames.</span></span> <span data-ttu-id="a2321-113">Это может улучшить качество очень шумных видеороликов, но может привести к тому, что в случае чистого видео в исходном видеоролике могут возникнуть помехи (также известные как конечные артефакты).</span><span class="sxs-lookup"><span data-stu-id="a2321-113">This can improve the quality of very noisy video, but can lead to motion trails (also known as trailing artifacts) when applied to clean source video.</span></span>

<span data-ttu-id="a2321-114">По умолчанию кодек использует внутреннюю логику, чтобы определить, следует ли использовать медианную фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="a2321-114">By default, the codec uses internal logic to determine whether median filtering should be used.</span></span> <span data-ttu-id="a2321-115">Если задать это свойство, эта логика будет переопределена.</span><span class="sxs-lookup"><span data-stu-id="a2321-115">If you set this property, that logic will be overridden.</span></span>

> [!Note]  
> <span data-ttu-id="a2321-116">Этот фильтр отличается от фильтров нечеткого размытия, обнаруженных во многих приложениях для редактирования и последующей обработки видео.</span><span class="sxs-lookup"><span data-stu-id="a2321-116">This filter is not the same as median blur filters found in many video editing and post-processing applications.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2321-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a2321-117">Requirements</span></span>



| <span data-ttu-id="a2321-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a2321-118">Requirement</span></span> | <span data-ttu-id="a2321-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a2321-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2321-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2321-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a2321-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a2321-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2321-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2321-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a2321-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2321-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a2321-124">Header</span><span class="sxs-lookup"><span data-stu-id="a2321-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2321-125"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2321-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2321-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2321-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2321-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2321-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




