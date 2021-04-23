---
description: В этом разделе перечислены методы Савеадд класса Image. Полный список методов для класса Image см. в разделе методы изображения.
ms.assetid: e597f6e6-6e07-4afb-8905-26e4af961685
title: Методы Image. Савеадд (Гдиплушеадерс. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a2b65c6fe56507538f092edc7128497de5cb2f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985317"
---
# <a name="imagesaveadd-methods"></a><span data-ttu-id="afa73-104">Методы Image. Савеадд</span><span class="sxs-lookup"><span data-stu-id="afa73-104">Image.SaveAdd methods</span></span>

<span data-ttu-id="afa73-105">В этом разделе перечислены методы Савеадд класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="afa73-105">This topic lists the SaveAdd methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="afa73-106">Полный список методов для класса **Image** см. в разделе [методы изображения](-gdiplus-class-image-methods.md).</span><span class="sxs-lookup"><span data-stu-id="afa73-106">For a complete list of methods for the **Image** class, see [Image Methods](-gdiplus-class-image-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="afa73-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="afa73-107">Overload list</span></span>



| <span data-ttu-id="afa73-108">Метод</span><span class="sxs-lookup"><span data-stu-id="afa73-108">Method</span></span>                                                                                               | <span data-ttu-id="afa73-109">Описание</span><span class="sxs-lookup"><span data-stu-id="afa73-109">Description</span></span>                                                                                                                                                                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa73-110">[**Савеадд (EncoderParameters \* )**](/previous-versions//ms535408(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="afa73-110">[**SaveAdd(EncoderParameters\*)**](/previous-versions//ms535408(v=vs.85))</span></span>                  | <span data-ttu-id="afa73-111">Метод [**Image:: савеадд**](/previous-versions//ms535408(v=vs.85)) добавляет кадр в файл или поток, указанный в предыдущем вызове метода **Save** .</span><span class="sxs-lookup"><span data-stu-id="afa73-111">The [**Image::SaveAdd**](/previous-versions//ms535408(v=vs.85)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span> <span data-ttu-id="afa73-112">Используйте данный метод для сохранения выбранных кадров из многокадрового изображения в другое многокадровое изображение.</span><span class="sxs-lookup"><span data-stu-id="afa73-112">Use this method to save selected frames from a multiple-frame image to another multiple-frame image.</span></span><br/> |
| <span data-ttu-id="afa73-113">[**Савеадд (изображение \* , EncoderParameters \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span><span class="sxs-lookup"><span data-stu-id="afa73-113">[**SaveAdd(Image\*,EncoderParameters\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span></span> | <span data-ttu-id="afa73-114">Метод [**Image:: савеадд**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) добавляет кадр в файл или поток, указанный в предыдущем вызове метода **Save** .</span><span class="sxs-lookup"><span data-stu-id="afa73-114">The [**Image::SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span><br/>                                                                                             |



## <a name="requirements"></a><span data-ttu-id="afa73-115">Требования</span><span class="sxs-lookup"><span data-stu-id="afa73-115">Requirements</span></span>



| <span data-ttu-id="afa73-116">Требование</span><span class="sxs-lookup"><span data-stu-id="afa73-116">Requirement</span></span> | <span data-ttu-id="afa73-117">Значение</span><span class="sxs-lookup"><span data-stu-id="afa73-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa73-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afa73-118">Minimum supported client</span></span><br/> | <span data-ttu-id="afa73-119">Windows XP, \[ только для настольных приложений windows 2000 Professional\]</span><span class="sxs-lookup"><span data-stu-id="afa73-119">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="afa73-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afa73-120">Minimum supported server</span></span><br/> | <span data-ttu-id="afa73-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="afa73-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="afa73-122">Продукт</span><span class="sxs-lookup"><span data-stu-id="afa73-122">Product</span></span><br/>                  | <span data-ttu-id="afa73-123">GDI+ 1,0</span><span class="sxs-lookup"><span data-stu-id="afa73-123">GDI+ 1.0</span></span><br/>                                                                                             |
| <span data-ttu-id="afa73-124">Header</span><span class="sxs-lookup"><span data-stu-id="afa73-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa73-125"><dt>Гдиплушеадерс. h (включение GDIPLUS. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afa73-125"><dt>Gdiplusheaders.h (include Gdiplus.h)</dt></span></span> </dl> |
| <span data-ttu-id="afa73-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="afa73-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="afa73-127"><dt>GDIPLUS. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afa73-127"><dt>Gdiplus.lib</dt></span></span> </dl>                          |



 

 
