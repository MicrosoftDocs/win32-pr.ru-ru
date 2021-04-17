---
title: Методы ID2D1DeviceContext2 Креатеимажесаурцефромвик (D2d1 \_ 3. h)
description: Создает исходный объект изображения из источника битовой карты WIC, заполняя всю память в пикселях в источнике изображения. Образ загружается и сохраняется с минимальным объемом памяти.
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
keywords:
- Методы Креатеимажесаурцефромвик Direct2D
topic_type:
- apiref
api_location:
- d2d1_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 20773912886840a185e1b9fc71576f89e9a40fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679929"
---
# <a name="id2d1devicecontext2createimagesourcefromwic-methods"></a><span data-ttu-id="f7bb3-105">Методы ID2D1DeviceContext2:: Креатеимажесаурцефромвик</span><span class="sxs-lookup"><span data-stu-id="f7bb3-105">ID2D1DeviceContext2::CreateImageSourceFromWic methods</span></span>

<span data-ttu-id="f7bb3-106">Создает исходный объект изображения из источника битовой карты WIC, заполняя всю память в пикселях в источнике изображения.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-106">Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.</span></span> <span data-ttu-id="f7bb3-107">Образ загружается и сохраняется с минимальным объемом памяти.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-107">The image is loaded and stored while using a minimal amount of memory.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f7bb3-108">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="f7bb3-108">Overload list</span></span>



| <span data-ttu-id="f7bb3-109">Метод</span><span class="sxs-lookup"><span data-stu-id="f7bb3-109">Method</span></span>                                                                                                                                                                                       | <span data-ttu-id="f7bb3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f7bb3-110">Description</span></span>                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7bb3-111">[**Креатеимажесаурцефромвик (IWICBitmapSource \* , \_ \_ Параметры загрузки источника изображения D2D1 \_ \_ , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="f7bb3-111">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span></span>                   | <span data-ttu-id="f7bb3-112">Версия метода, позволяющая указать источник битовой карты WIC, исходный объект выходного изображения и параметры загрузки в режиме альфа-канала по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-112">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options with default alpha mode.</span></span><br/>   |
| <span data-ttu-id="f7bb3-113">[**Креатеимажесаурцефромвик (IWICBitmapSource \* , \_ \_ Параметры загрузки источника изображения D2D1 \_ \_ , \_ режим альфа \_ -канала D2D1, ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="f7bb3-113">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, D2D1\_ALPHA\_MODE, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span></span> | <span data-ttu-id="f7bb3-114">Версия метода, позволяющая указать источник битовой карты WIC, исходный объект выходного изображения, параметры загрузки и режим альфа.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-114">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options, and alpha mode.</span></span><br/>           |
| <span data-ttu-id="f7bb3-115">[**Креатеимажесаурцефромвик (IWICBitmapSource \* , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="f7bb3-115">[**CreateImageSourceFromWic (IWICBitmapSource\*, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span></span>                                                          | <span data-ttu-id="f7bb3-116">Версия метода, позволяющая указать источник битовой карты WIC и исходный объект выходного изображения с загрузкой опитонс и режимом альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-116">Version of the method that allows you to specify the WIC bitmap source and the output image source object with default loading opitons and alpha mode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f7bb3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f7bb3-117">Requirements</span></span>



| <span data-ttu-id="f7bb3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f7bb3-118">Requirement</span></span> | <span data-ttu-id="f7bb3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f7bb3-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7bb3-120">Header</span><span class="sxs-lookup"><span data-stu-id="f7bb3-120">Header</span></span><br/> | <dl> <span data-ttu-id="f7bb3-121"><dt>D2d1 \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7bb3-121"><dt>D2d1\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7bb3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7bb3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7bb3-123">**ID2D1DeviceContext2**</span><span class="sxs-lookup"><span data-stu-id="f7bb3-123">**ID2D1DeviceContext2**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2)
</dt> </dl>

<span data-ttu-id="f7bb3-124">�</span><span class="sxs-lookup"><span data-stu-id="f7bb3-124">�</span></span>

<span data-ttu-id="f7bb3-125">�</span><span class="sxs-lookup"><span data-stu-id="f7bb3-125">�</span></span>
