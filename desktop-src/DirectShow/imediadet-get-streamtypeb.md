---
description: Метод Get \_ стреамтипеб извлекает строку, представляющую идентификатор GUID типа носителя для текущего потока.
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: 'Метод Имедиадет:: get_StreamTypeB (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamTypeB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd1cdf4bbadfa769654f20792cf2fda17dbe2806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679781"
---
# <a name="imediadetget_streamtypeb-method"></a><span data-ttu-id="aad01-103">Метод Имедиадет:: Get \_ стреамтипеб</span><span class="sxs-lookup"><span data-stu-id="aad01-103">IMediaDet::get\_StreamTypeB method</span></span>

> [!Note]  
> <span data-ttu-id="aad01-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="aad01-104">\[Deprecated.</span></span> <span data-ttu-id="aad01-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aad01-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aad01-106">`get_StreamTypeB`Метод получает строку, представляющую идентификатор GUID типа носителя для текущего потока.</span><span class="sxs-lookup"><span data-stu-id="aad01-106">The `get_StreamTypeB` method retrieves a string representing the GUID of the media type for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad01-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aad01-107">Syntax</span></span>


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="aad01-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aad01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aad01-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="aad01-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="aad01-110">Получает строковое представление идентификатора GUID типа носителя.</span><span class="sxs-lookup"><span data-stu-id="aad01-110">Receives a string representation of the media type GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aad01-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aad01-111">Return value</span></span>

<span data-ttu-id="aad01-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="aad01-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aad01-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aad01-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aad01-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aad01-114">Remarks</span></span>

<span data-ttu-id="aad01-115">Возвращаемая **BSTR** форматируется следующим образом: `{73647561-0000-0010-8000-00AA00389B71}`</span><span class="sxs-lookup"><span data-stu-id="aad01-115">The returned **BSTR** is formatted like the following: `{73647561-0000-0010-8000-00AA00389B71}`</span></span>

<span data-ttu-id="aad01-116">Метод выделяет память для строки.</span><span class="sxs-lookup"><span data-stu-id="aad01-116">The method allocates memory for the string.</span></span> <span data-ttu-id="aad01-117">Приложение должно вызвать **сисфристринг** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="aad01-117">The application must call **SysFreeString** to free the memory.</span></span>

<span data-ttu-id="aad01-118">Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="aad01-118">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="aad01-119">Если средство обнаружения мультимедиа находится в режиме захвата растрового изображения, этот метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="aad01-119">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="aad01-120">Дополнительные сведения см. в разделе [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="aad01-120">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="aad01-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="aad01-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aad01-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aad01-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aad01-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="aad01-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aad01-124">Требования</span><span class="sxs-lookup"><span data-stu-id="aad01-124">Requirements</span></span>



| <span data-ttu-id="aad01-125">Требование</span><span class="sxs-lookup"><span data-stu-id="aad01-125">Requirement</span></span> | <span data-ttu-id="aad01-126">Значение</span><span class="sxs-lookup"><span data-stu-id="aad01-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aad01-127">Header</span><span class="sxs-lookup"><span data-stu-id="aad01-127">Header</span></span><br/>  | <dl> <span data-ttu-id="aad01-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="aad01-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aad01-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aad01-129">Library</span></span><br/> | <dl> <span data-ttu-id="aad01-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aad01-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aad01-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aad01-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad01-132">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="aad01-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="aad01-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="aad01-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




