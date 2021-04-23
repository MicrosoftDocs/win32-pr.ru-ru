---
description: Метод Жетбитмапбитс извлекает кадр видео в указанное время носителя. Возвращаемый кадр всегда находится в 24-разрядном формате RGB.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'Метод Имедиадет:: Жетбитмапбитс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679780"
---
# <a name="imediadetgetbitmapbits-method"></a><span data-ttu-id="36d52-104">Метод Имедиадет:: Жетбитмапбитс</span><span class="sxs-lookup"><span data-stu-id="36d52-104">IMediaDet::GetBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="36d52-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="36d52-105">\[Deprecated.</span></span> <span data-ttu-id="36d52-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36d52-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="36d52-107">`GetBitmapBits`Метод извлекает кадр видео в указанное время носителя.</span><span class="sxs-lookup"><span data-stu-id="36d52-107">The `GetBitmapBits` method retrieves a video frame at the specified media time.</span></span> <span data-ttu-id="36d52-108">Возвращаемый кадр всегда находится в 24-разрядном формате RGB.</span><span class="sxs-lookup"><span data-stu-id="36d52-108">The returned frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d52-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36d52-109">Syntax</span></span>


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a><span data-ttu-id="36d52-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="36d52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36d52-111">*стреамтиме*</span><span class="sxs-lookup"><span data-stu-id="36d52-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="36d52-112">Время получения кадра видео в секундах.</span><span class="sxs-lookup"><span data-stu-id="36d52-112">Time at which to retrieve the video frame, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="36d52-113">*пбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="36d52-113">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="36d52-114">Получает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="36d52-114">Receives the required buffer size.</span></span> <span data-ttu-id="36d52-115">Если *pBuffer* имеет **значение NULL**, переменная получает размер буфера, необходимого для получения кадра.</span><span class="sxs-lookup"><span data-stu-id="36d52-115">If *pBuffer* is **NULL**, the variable receives the size of the buffer needed to retrieve the frame.</span></span> <span data-ttu-id="36d52-116">Если *pBuffer* не равно **null**, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="36d52-116">If *pBuffer* is not **NULL**, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="36d52-117">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="36d52-117">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="36d52-118">Указатель на буфер, который получает структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , за которой СЛЕДУЮТ биты DIB.</span><span class="sxs-lookup"><span data-stu-id="36d52-118">Pointer to a buffer that receives a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the DIB bits.</span></span>

</dd> <dt>

<span data-ttu-id="36d52-119">*Width*</span><span class="sxs-lookup"><span data-stu-id="36d52-119">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="36d52-120">Ширина изображения видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="36d52-120">Width of the video image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="36d52-121">*Height*</span><span class="sxs-lookup"><span data-stu-id="36d52-121">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="36d52-122">Высота изображения видео (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="36d52-122">Height of the video image, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36d52-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36d52-123">Return value</span></span>

<span data-ttu-id="36d52-124">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36d52-124">Returns an **HRESULT** value.</span></span> <span data-ttu-id="36d52-125">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="36d52-125">Possible values include the following:</span></span>



| <span data-ttu-id="36d52-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="36d52-126">Return code</span></span>                                                                                             | <span data-ttu-id="36d52-127">Описание</span><span class="sxs-lookup"><span data-stu-id="36d52-127">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36d52-128"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="36d52-128"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="36d52-129">Успешно.</span><span class="sxs-lookup"><span data-stu-id="36d52-129">Success.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="36d52-130"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="36d52-130"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="36d52-131">Не удалось добавить [**образец фильтра захвата**](sample-grabber-filter.md) к диаграмме.</span><span class="sxs-lookup"><span data-stu-id="36d52-131">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="36d52-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="36d52-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="36d52-133">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="36d52-133">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="36d52-134"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="36d52-134"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="36d52-135">Ошибка указателя **null** .</span><span class="sxs-lookup"><span data-stu-id="36d52-135">**NULL** pointer error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="36d52-136"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="36d52-136"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="36d52-137">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="36d52-137">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="36d52-138"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="36d52-138"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="36d52-139">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="36d52-139">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="36d52-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36d52-140">Remarks</span></span>

<span data-ttu-id="36d52-141">Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="36d52-141">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="36d52-142">Чтобы определить необходимый размер буфера, вызовите этот метод с *pBuffer* , равным **null**.</span><span class="sxs-lookup"><span data-stu-id="36d52-142">To determine the size of the buffer that is required, call this method with *pBuffer* equal to **NULL**.</span></span> <span data-ttu-id="36d52-143">Размер возвращается в переменную, на которую указывает *пбуфферсизе*.</span><span class="sxs-lookup"><span data-stu-id="36d52-143">The size is returned in the variable pointed to by *pBufferSize*.</span></span> <span data-ttu-id="36d52-144">Затем создайте буфер и снова вызовите метод с *pBuffer* , равным адресу буфера.</span><span class="sxs-lookup"><span data-stu-id="36d52-144">Then create the buffer and call the method again, with *pBuffer* equal to the address of the buffer.</span></span> <span data-ttu-id="36d52-145">Когда метод возвращает значение, буфер содержит структуру **битмапинфохеадер** , за которой следует точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="36d52-145">When the method returns, the buffer contains a **BITMAPINFOHEADER** structure followed by the bitmap.</span></span> <span data-ttu-id="36d52-146">Битовая карта масштабируется по измерениям, указанным в параметрах *Width* и *Height* .</span><span class="sxs-lookup"><span data-stu-id="36d52-146">The bitmap is scaled to the dimensions specified in the *Width* and *Height* parameters.</span></span>

<span data-ttu-id="36d52-147">Этот метод помещает средство обнаружения мультимедиа в режим захвата точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="36d52-147">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="36d52-148">После вызова этого метода различные методы потоковой информации в **имедиадет** не работают, если не создать новый экземпляр детектора мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="36d52-148">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="36d52-149">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="36d52-149">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="36d52-150">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="36d52-150">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="36d52-151">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="36d52-151">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="36d52-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="36d52-152">Examples</span></span>

<span data-ttu-id="36d52-153">В следующем коде используется `GetBitmapBits` метод для создания аппаратно-независимого точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="36d52-153">The following code uses the `GetBitmapBits` method to create a device-independent bitmap.</span></span>


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a><span data-ttu-id="36d52-154">Требования</span><span class="sxs-lookup"><span data-stu-id="36d52-154">Requirements</span></span>



| <span data-ttu-id="36d52-155">Требование</span><span class="sxs-lookup"><span data-stu-id="36d52-155">Requirement</span></span> | <span data-ttu-id="36d52-156">Значение</span><span class="sxs-lookup"><span data-stu-id="36d52-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36d52-157">Header</span><span class="sxs-lookup"><span data-stu-id="36d52-157">Header</span></span><br/>  | <dl> <span data-ttu-id="36d52-158"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="36d52-158"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="36d52-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36d52-159">Library</span></span><br/> | <dl> <span data-ttu-id="36d52-160"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36d52-160"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36d52-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36d52-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d52-162">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="36d52-162">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="36d52-163">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="36d52-163">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




