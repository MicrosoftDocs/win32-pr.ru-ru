---
description: Интерфейс Идкстжпег задает свойства для перехода на очистку SMPTE. Этот интерфейс внутренне используется службами редактирования DirectShow (DES) при визуализации перехода на очистку SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Интерфейс Идкстжпег (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675331"
---
# <a name="idxtjpeg-interface"></a><span data-ttu-id="73980-103">Интерфейс Идкстжпег</span><span class="sxs-lookup"><span data-stu-id="73980-103">IDxtJpeg interface</span></span>

> [!Note]  
> <span data-ttu-id="73980-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="73980-104">\[Deprecated.</span></span> <span data-ttu-id="73980-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="73980-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="73980-106">`IDxtJpeg`Интерфейс задает свойства для перехода на [очистку SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="73980-106">The `IDxtJpeg` interface sets properties on the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

<span data-ttu-id="73980-107">Этот интерфейс внутренне используется службами редактирования DirectShow (DES) при визуализации перехода на очистку SMPTE.</span><span class="sxs-lookup"><span data-stu-id="73980-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the SMPTE Wipe transition.</span></span> <span data-ttu-id="73980-108">Приложениям DES не требуется использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="73980-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="73980-109">Чтобы задать свойства для перехода в DES, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="73980-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="73980-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="73980-110">Members</span></span>

<span data-ttu-id="73980-111">Интерфейс **идкстжпег** наследует от **идксеффект**.</span><span class="sxs-lookup"><span data-stu-id="73980-111">The **IDxtJpeg** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="73980-112">**Идкстжпег** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="73980-112">**IDxtJpeg** also has these types of members:</span></span>

-   [<span data-ttu-id="73980-113">Методы</span><span class="sxs-lookup"><span data-stu-id="73980-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="73980-114">Методы</span><span class="sxs-lookup"><span data-stu-id="73980-114">Methods</span></span>

<span data-ttu-id="73980-115">Интерфейс **идкстжпег** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="73980-115">The **IDxtJpeg** interface has these methods.</span></span>



| <span data-ttu-id="73980-116">Метод</span><span class="sxs-lookup"><span data-stu-id="73980-116">Method</span></span>                                                     | <span data-ttu-id="73980-117">Описание</span><span class="sxs-lookup"><span data-stu-id="73980-117">Description</span></span>                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73980-118">**ApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="73980-118">**ApplyChanges**</span></span>](idxtjpeg-applychanges.md)              | <span data-ttu-id="73980-119">Применяет все измененные свойства.</span><span class="sxs-lookup"><span data-stu-id="73980-119">Applies any properties that have changed.</span></span><br/>                                      |
| [<span data-ttu-id="73980-120">**получить \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="73980-120">**get\_BorderColor**</span></span>](idxtjpeg-get-bordercolor.md)       | <span data-ttu-id="73980-121">Получает цвет границы вокруг границ шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-121">Retrieves the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="73980-122">**получить \_ бордерсофтнесс**</span><span class="sxs-lookup"><span data-stu-id="73980-122">**get\_BorderSoftness**</span></span>](idxtjpeg-get-bordersoftness.md) | <span data-ttu-id="73980-123">Получает ширину размытой области вокруг краев шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-123">Retrieves the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="73980-124">**получить \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="73980-124">**get\_BorderWidth**</span></span>](idxtjpeg-get-borderwidth.md)       | <span data-ttu-id="73980-125">Получает ширину сплошной границы вдоль краев шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-125">Retrieves the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="73980-126">**получить \_ маскнаме**</span><span class="sxs-lookup"><span data-stu-id="73980-126">**get\_MaskName**</span></span>](idxtjpeg-get-maskname.md)             | <span data-ttu-id="73980-127">Извлекает имя JPEG-файла, который будет использоваться в качестве маски очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-127">Retrieves the name of a JPEG file to be used as the wipe mask.</span></span><br/>                 |
| [<span data-ttu-id="73980-128">**получить \_ маскнум**</span><span class="sxs-lookup"><span data-stu-id="73980-128">**get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)               | <span data-ttu-id="73980-129">Извлекает код очистки SMPTE.</span><span class="sxs-lookup"><span data-stu-id="73980-129">Retrieves the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="73980-130">**получить \_ оффсеткс**</span><span class="sxs-lookup"><span data-stu-id="73980-130">**get\_OffsetX**</span></span>](idxtjpeg-get-offsetx.md)               | <span data-ttu-id="73980-131">Возвращает горизонтальное смещение начала очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-131">Retrieves the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="73980-132">**получить \_ смещение**</span><span class="sxs-lookup"><span data-stu-id="73980-132">**get\_OffsetY**</span></span>](idxtjpeg-get-offsety.md)               | <span data-ttu-id="73980-133">Получает вертикальное смещение источника очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-133">Retrieves the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="73980-134">**получить \_ репликатекс**</span><span class="sxs-lookup"><span data-stu-id="73980-134">**get\_ReplicateX**</span></span>](idxtjpeg-get-replicatex.md)         | <span data-ttu-id="73980-135">Извлекает количество раз, когда шаблон очистки реплицируется по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="73980-135">Retrieves the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="73980-136">**получить \_ репликацию**</span><span class="sxs-lookup"><span data-stu-id="73980-136">**get\_ReplicateY**</span></span>](idxtjpeg-get-replicatey.md)         | <span data-ttu-id="73980-137">Извлекает количество раз, когда шаблон очистки реплицируется по вертикали.</span><span class="sxs-lookup"><span data-stu-id="73980-137">Retrieves the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="73980-138">**получение \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="73980-138">**get\_ScaleX**</span></span>](idxtjpeg-get-scalex.md)                 | <span data-ttu-id="73980-139">Возвращает величину, на которую производится растяжение очистки по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="73980-139">Retrieves the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="73980-140">**получить \_ масштабирование**</span><span class="sxs-lookup"><span data-stu-id="73980-140">**get\_ScaleY**</span></span>](idxtjpeg-get-scaley.md)                 | <span data-ttu-id="73980-141">Возвращает величину, на которую производится растяжение очистки по вертикали.</span><span class="sxs-lookup"><span data-stu-id="73980-141">Retrieves the amount by which the wipe is stretched vertically.</span></span><br/>                |
| [<span data-ttu-id="73980-142">**лоаддефсеттингс**</span><span class="sxs-lookup"><span data-stu-id="73980-142">**LoadDefSettings**</span></span>](idxtjpeg-loaddefsettings.md)        | <span data-ttu-id="73980-143">Восстанавливает параметры по умолчанию для перехода на очистку.</span><span class="sxs-lookup"><span data-stu-id="73980-143">Restores the default settings of the Wipe transition.</span></span><br/>                          |
| [<span data-ttu-id="73980-144">**вставить \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="73980-144">**put\_BorderColor**</span></span>](idxtjpeg-put-bordercolor.md)       | <span data-ttu-id="73980-145">Задает цвет границы вокруг границ шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-145">Specifies the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="73980-146">**разместить \_ бордерсофтнесс**</span><span class="sxs-lookup"><span data-stu-id="73980-146">**put\_BorderSoftness**</span></span>](idxtjpeg-put-bordersoftness.md) | <span data-ttu-id="73980-147">Задает ширину размытой области вокруг краев шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-147">Specifies the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="73980-148">**разместить \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="73980-148">**put\_BorderWidth**</span></span>](idxtjpeg-put-borderwidth.md)       | <span data-ttu-id="73980-149">Задает ширину сплошной границы вдоль краев шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-149">Specifies the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="73980-150">**разместить \_ маскнаме**</span><span class="sxs-lookup"><span data-stu-id="73980-150">**put\_MaskName**</span></span>](idxtjpeg-put-maskname.md)             | <span data-ttu-id="73980-151">Указывает имя JPEG-файла, используемого в качестве маски очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-151">Specifies the name of a JPEG file to use as the wipe mask.</span></span><br/>                     |
| [<span data-ttu-id="73980-152">**разместить \_ маскнум**</span><span class="sxs-lookup"><span data-stu-id="73980-152">**put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)               | <span data-ttu-id="73980-153">Указывает код очистки SMPTE.</span><span class="sxs-lookup"><span data-stu-id="73980-153">Specifies the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="73980-154">**разместить \_ оффсеткс**</span><span class="sxs-lookup"><span data-stu-id="73980-154">**put\_OffsetX**</span></span>](idxtjpeg-put-offsetx.md)               | <span data-ttu-id="73980-155">Задает горизонтальное смещение источника очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-155">Specifies the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="73980-156">**разместить \_ смещение**</span><span class="sxs-lookup"><span data-stu-id="73980-156">**put\_OffsetY**</span></span>](idxtjpeg-put-offsety.md)               | <span data-ttu-id="73980-157">Задает вертикальное смещение источника очистки.</span><span class="sxs-lookup"><span data-stu-id="73980-157">Specifies the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="73980-158">**разместить \_ репликатекс**</span><span class="sxs-lookup"><span data-stu-id="73980-158">**put\_ReplicateX**</span></span>](idxtjpeg-put-replicatex.md)         | <span data-ttu-id="73980-159">Указывает, сколько раз шаблон очистки реплицируется по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="73980-159">Specifies the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="73980-160">**разместить \_ репликацию**</span><span class="sxs-lookup"><span data-stu-id="73980-160">**put\_ReplicateY**</span></span>](idxtjpeg-put-replicatey.md)         | <span data-ttu-id="73980-161">Указывает, сколько раз шаблон очистки реплицируется по вертикали.</span><span class="sxs-lookup"><span data-stu-id="73980-161">Specifies the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="73980-162">**Размещение \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="73980-162">**put\_ScaleX**</span></span>](idxtjpeg-put-scalex.md)                 | <span data-ttu-id="73980-163">Указывает величину, на которую производится растяжение очистки по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="73980-163">Specifies the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="73980-164">**разместить \_ масштаб**</span><span class="sxs-lookup"><span data-stu-id="73980-164">**put\_ScaleY**</span></span>](idxtjpeg-put-scaley.md)                 | <span data-ttu-id="73980-165">Указывает величину, на которую производится растяжение очистки по вертикали.</span><span class="sxs-lookup"><span data-stu-id="73980-165">Specifies the amount by which the wipe is stretched vertically.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="73980-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73980-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73980-167">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="73980-167">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="73980-168">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="73980-168">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="73980-169">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="73980-169">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73980-170">Требования</span><span class="sxs-lookup"><span data-stu-id="73980-170">Requirements</span></span>



| <span data-ttu-id="73980-171">Требование</span><span class="sxs-lookup"><span data-stu-id="73980-171">Requirement</span></span> | <span data-ttu-id="73980-172">Значение</span><span class="sxs-lookup"><span data-stu-id="73980-172">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73980-173">Header</span><span class="sxs-lookup"><span data-stu-id="73980-173">Header</span></span><br/>  | <dl> <span data-ttu-id="73980-174"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="73980-174"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="73980-175">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73980-175">Library</span></span><br/> | <dl> <span data-ttu-id="73980-176"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73980-176"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




