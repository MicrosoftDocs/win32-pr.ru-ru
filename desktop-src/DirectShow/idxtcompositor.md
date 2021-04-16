---
description: Интерфейс Идксткомпоситор задает свойства для перехода компоновщика. Этот интерфейс внутренне используется службами редактирования DirectShow (DES) при визуализации перехода компоновщика.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Интерфейс Идксткомпоситор (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679716"
---
# <a name="idxtcompositor-interface"></a><span data-ttu-id="4c8bc-103">Интерфейс Идксткомпоситор</span><span class="sxs-lookup"><span data-stu-id="4c8bc-103">IDxtCompositor interface</span></span>

> [!Note]  
> <span data-ttu-id="4c8bc-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-104">\[Deprecated.</span></span> <span data-ttu-id="4c8bc-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c8bc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c8bc-106">`IDxtCompositor`Интерфейс задает свойства для перехода [компоновщика](compositor-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="4c8bc-106">The `IDxtCompositor` interface sets properties on the [Compositor](compositor-transition.md) transition.</span></span>

<span data-ttu-id="4c8bc-107">Этот интерфейс внутренне используется службами редактирования DirectShow (DES) при визуализации перехода компоновщика.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Compositor transition.</span></span> <span data-ttu-id="4c8bc-108">Приложениям DES не требуется использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="4c8bc-109">Чтобы задать свойства для перехода в DES, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="4c8bc-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="4c8bc-110">Переход с помощью компоновщика комбинирует изображение переднего плана на фоновое изображение.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-110">The Compositor transition composites a foreground image onto a background image.</span></span> <span data-ttu-id="4c8bc-111">*Исходный прямоугольник* определяет раздел составного изображения.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-111">The *source rectangle* defines the section of the foreground image that is composited.</span></span> <span data-ttu-id="4c8bc-112">*Прямоугольник назначения* определяет раздел фонового изображения, получающего изображение переднего плана.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-112">The *destination rectangle* defines the section of the background image that receives the foreground image.</span></span> <span data-ttu-id="4c8bc-113">Эти прямоугольники показаны на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-113">The following diagram illustrates these rectangles.</span></span>

![Свойства перехода для компоновщика](images/compmeasure.png)

## <a name="members"></a><span data-ttu-id="4c8bc-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="4c8bc-115">Members</span></span>

<span data-ttu-id="4c8bc-116">Интерфейс **идксткомпоситор** наследует от **идксеффект**.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-116">The **IDxtCompositor** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="4c8bc-117">**Идксткомпоситор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4c8bc-117">**IDxtCompositor** also has these types of members:</span></span>

-   [<span data-ttu-id="4c8bc-118">Методы</span><span class="sxs-lookup"><span data-stu-id="4c8bc-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4c8bc-119">Методы</span><span class="sxs-lookup"><span data-stu-id="4c8bc-119">Methods</span></span>

<span data-ttu-id="4c8bc-120">Интерфейс **идксткомпоситор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-120">The **IDxtCompositor** interface has these methods.</span></span>



| <span data-ttu-id="4c8bc-121">Метод</span><span class="sxs-lookup"><span data-stu-id="4c8bc-121">Method</span></span>                                                   | <span data-ttu-id="4c8bc-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4c8bc-122">Description</span></span>                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="4c8bc-123">**получить \_ высоту**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-123">**get\_Height**</span></span>](idxtcompositor-get-height.md)         | <span data-ttu-id="4c8bc-124">Получает высоту целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-124">Retrieves the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="4c8bc-125">**получить \_ оффсеткс**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-125">**get\_OffsetX**</span></span>](idxtcompositor-get-offsetx.md)       | <span data-ttu-id="4c8bc-126">Возвращает горизонтальное смещение целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-126">Retrieves the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="4c8bc-127">**получить \_ смещение**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-127">**get\_OffsetY**</span></span>](idxtcompositor-get-offsety.md)       | <span data-ttu-id="4c8bc-128">Получает вертикальное смещение целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-128">Retrieves the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="4c8bc-129">**получить \_ срчеигхт**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-129">**get\_SrcHeight**</span></span>](idxtcompositor-get-srcheight.md)   | <span data-ttu-id="4c8bc-130">Получает высоту исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-130">Retrieves the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="4c8bc-131">**получить \_ сркоффсеткс**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-131">**get\_SrcOffsetX**</span></span>](idxtcompositor-get-srcoffsetx.md) | <span data-ttu-id="4c8bc-132">Возвращает горизонтальное смещение исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-132">Retrieves the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="4c8bc-133">**получить \_ сркоффсети**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-133">**get\_SrcOffsetY**</span></span>](idxtcompositor-get-srcoffsety.md) | <span data-ttu-id="4c8bc-134">Возвращает вертикальное смещение исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-134">Retrieves the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="4c8bc-135">**получить \_ срквидс**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-135">**get\_SrcWidth**</span></span>](idxtcompositor-get-srcwidth.md)     | <span data-ttu-id="4c8bc-136">Возвращает ширину исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-136">Retrieves the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="4c8bc-137">**получить \_ ширину**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-137">**get\_Width**</span></span>](idxtcompositor-get-width.md)           | <span data-ttu-id="4c8bc-138">Получает ширину целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-138">Retrieves the width of the target rectangle.</span></span><br/>             |
| [<span data-ttu-id="4c8bc-139">**вставить \_ высоту**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-139">**put\_Height**</span></span>](idxtcompositor-put-height.md)         | <span data-ttu-id="4c8bc-140">Задает высоту целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-140">Specifies the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="4c8bc-141">**разместить \_ оффсеткс**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-141">**put\_OffsetX**</span></span>](idxtcompositor-put-offsetx.md)       | <span data-ttu-id="4c8bc-142">Задает горизонтальное смещение целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-142">Specifies the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="4c8bc-143">**разместить \_ смещение**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-143">**put\_OffsetY**</span></span>](idxtcompositor-put-offsety.md)       | <span data-ttu-id="4c8bc-144">Задает вертикальное смещение целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-144">Specifies the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="4c8bc-145">**разместить \_ срчеигхт**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-145">**put\_SrcHeight**</span></span>](idxtcompositor-put-srcheight.md)   | <span data-ttu-id="4c8bc-146">Задает высоту исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-146">Specifies the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="4c8bc-147">**разместить \_ сркоффсеткс**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-147">**put\_SrcOffsetX**</span></span>](idxtcompositor-put-srcoffsetx.md) | <span data-ttu-id="4c8bc-148">Задает горизонтальное смещение исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-148">Specifies the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="4c8bc-149">**разместить \_ сркоффсети**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-149">**put\_SrcOffsetY**</span></span>](idxtcompositor-put-srcoffsety.md) | <span data-ttu-id="4c8bc-150">Задает вертикальное смещение исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-150">Specifies the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="4c8bc-151">**разместить \_ срквидс**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-151">**put\_SrcWidth**</span></span>](idxtcompositor-put-srcwidth.md)     | <span data-ttu-id="4c8bc-152">Задает ширину исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-152">Specifies the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="4c8bc-153">**вставить \_ ширину**</span><span class="sxs-lookup"><span data-stu-id="4c8bc-153">**put\_Width**</span></span>](idxtcompositor-put-width.md)           | <span data-ttu-id="4c8bc-154">Задает ширину целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-154">Specifies the width of the target rectangle.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="4c8bc-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c8bc-155">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c8bc-156">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4c8bc-156">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c8bc-157">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c8bc-157">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c8bc-158">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4c8bc-158">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c8bc-159">Требования</span><span class="sxs-lookup"><span data-stu-id="4c8bc-159">Requirements</span></span>



| <span data-ttu-id="4c8bc-160">Требование</span><span class="sxs-lookup"><span data-stu-id="4c8bc-160">Requirement</span></span> | <span data-ttu-id="4c8bc-161">Значение</span><span class="sxs-lookup"><span data-stu-id="4c8bc-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8bc-162">Header</span><span class="sxs-lookup"><span data-stu-id="4c8bc-162">Header</span></span><br/>  | <dl> <span data-ttu-id="4c8bc-163"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c8bc-163"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c8bc-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4c8bc-164">Library</span></span><br/> | <dl> <span data-ttu-id="4c8bc-165"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c8bc-165"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




