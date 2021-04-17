---
title: ID2D1Factory Креатевикбитмапрендертаржет методы
description: Создает целевой объект отрисовки, который визуализируется в виде растрового изображения компонента Microsoft Windows Imaging Component (WIC).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Методы Креатевикбитмапрендертаржет Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657049"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a><span data-ttu-id="60997-104">Методы ID2D1Factory:: Креатевикбитмапрендертаржет</span><span class="sxs-lookup"><span data-stu-id="60997-104">ID2D1Factory::CreateWicBitmapRenderTarget methods</span></span>

<span data-ttu-id="60997-105">Создает целевой объект отрисовки, который визуализируется в виде растрового изображения компонента Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="60997-105">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="60997-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="60997-106">Overload list</span></span>



| <span data-ttu-id="60997-107">Метод</span><span class="sxs-lookup"><span data-stu-id="60997-107">Method</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="60997-108">Описание</span><span class="sxs-lookup"><span data-stu-id="60997-108">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60997-109">[**Креатевикбитмапрендертаржет (Ивикбитмап \* , \_ \_ свойства целевого объекта прорисовки D2D1 \_ \* , ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="60997-109">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES\*,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span></span> | <span data-ttu-id="60997-110">Создает целевой объект отрисовки, который визуализируется в виде растрового изображения компонента Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="60997-110">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |
| <span data-ttu-id="60997-111">[**Креатевикбитмапрендертаржет (Ивикбитмап \* , \_ \_ свойства целевого объекта прорисовки D2D1 \_&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="60997-111">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES&,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span></span>  | <span data-ttu-id="60997-112">Создает целевой объект отрисовки, который визуализируется в виде растрового изображения компонента Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="60997-112">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="60997-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60997-113">Remarks</span></span>

<span data-ttu-id="60997-114">Приложение должно создавать целевые объекты рендеринга один раз и удерживать их на протяжении всего жизненного цикла приложения или до тех пор, пока не будет получено сообщение об ошибке [**\_ повторного создания \_ D2DERR**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="60997-114">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="60997-115">При возникновении этой ошибки необходимо повторно создать целевой объект рендеринга (и все созданные им ресурсы).</span><span class="sxs-lookup"><span data-stu-id="60997-115">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

<span data-ttu-id="60997-116">**Примечание**   .   Этот метод не поддерживается в Windows Phone и будет неудачным при вызове на устройстве с кодом ошибки 0x8899000b (для этой операции отсутствует устройство для отрисовки оборудования).</span><span class="sxs-lookup"><span data-stu-id="60997-116">**Note**   This method isn't supported on Windows Phone and will fail when called on a device with error code 0x8899000b ( There is no hardware rendering device available for this operation ).</span></span> <span data-ttu-id="60997-117">Так как эмулятор Windows Phone поддерживает отрисовку деформации, этот метод завершится ошибкой при вызове в эмуляторе с другим кодом ошибки 0x88982f80 (винкодек \_ Err \_ унсуппортедпикселформат).</span><span class="sxs-lookup"><span data-stu-id="60997-117">Because the Windows Phone Emulator supports WARP rendering, this method will fail when called on the emulator with a different error code, 0x88982f80 (wincodec\_err\_unsupportedpixelformat).</span></span>

## <a name="requirements"></a><span data-ttu-id="60997-118">Требования</span><span class="sxs-lookup"><span data-stu-id="60997-118">Requirements</span></span>



| <span data-ttu-id="60997-119">Требование</span><span class="sxs-lookup"><span data-stu-id="60997-119">Requirement</span></span> | <span data-ttu-id="60997-120">Значение</span><span class="sxs-lookup"><span data-stu-id="60997-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="60997-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="60997-121">Library</span></span><br/> | <dl> <span data-ttu-id="60997-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60997-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="60997-123">DLL</span><span class="sxs-lookup"><span data-stu-id="60997-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="60997-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60997-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60997-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60997-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60997-126">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="60997-126">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

