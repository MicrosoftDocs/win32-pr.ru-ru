---
description: Указывает объем содержимого в миллисекундах, который может поместиться в буфер модели.
ms.assetid: da959bef-1e87-4638-9a77-4135c31a3d27
title: Свойство MFPKEY_VIDEOWINDOW (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33d10b3a589ef3bcfc945b2c3404c7b02cb7121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543978"
---
# <a name="mfpkey_videowindow-property"></a><span data-ttu-id="fd2b3-103">МФПКЭЙ \_ видеовиндов, свойство</span><span class="sxs-lookup"><span data-stu-id="fd2b3-103">MFPKEY\_VIDEOWINDOW Property</span></span>

<span data-ttu-id="fd2b3-104">Указывает объем содержимого в миллисекундах, который может поместиться в буфер модели.</span><span class="sxs-lookup"><span data-stu-id="fd2b3-104">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fd2b3-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="fd2b3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fd2b3-106">g \_ всзвмвквидеовиндов</span><span class="sxs-lookup"><span data-stu-id="fd2b3-106">g\_wszWMVCVideoWIndow</span></span>

## <a name="data-type"></a><span data-ttu-id="fd2b3-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fd2b3-107">Data Type</span></span>

<span data-ttu-id="fd2b3-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fd2b3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="fd2b3-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fd2b3-109">Default Value</span></span>

<span data-ttu-id="fd2b3-110">3000</span><span class="sxs-lookup"><span data-stu-id="fd2b3-110">3000</span></span>

## <a name="remarks"></a><span data-ttu-id="fd2b3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd2b3-111">Remarks</span></span>

<span data-ttu-id="fd2b3-112">Окно буфера — это один из параметров модели «сегмент утечки», используемый для управления скоростью кодека.</span><span class="sxs-lookup"><span data-stu-id="fd2b3-112">The buffer window is one of the "leaky bucket" model parameters used in the codec rate control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd2b3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="fd2b3-113">Requirements</span></span>



| <span data-ttu-id="fd2b3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="fd2b3-114">Requirement</span></span> | <span data-ttu-id="fd2b3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fd2b3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2b3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd2b3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd2b3-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fd2b3-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fd2b3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd2b3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd2b3-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd2b3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd2b3-120">Header</span><span class="sxs-lookup"><span data-stu-id="fd2b3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd2b3-121"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd2b3-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd2b3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd2b3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2b3-123">Настройка кодирования видео</span><span class="sxs-lookup"><span data-stu-id="fd2b3-123">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="fd2b3-124">Модель буфера для контейнера утечки</span><span class="sxs-lookup"><span data-stu-id="fd2b3-124">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="fd2b3-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd2b3-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




