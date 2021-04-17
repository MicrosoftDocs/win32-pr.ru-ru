---
description: Метод Get \_ аутпутстреамс извлекает количество аудио и видеопотоков, содержащихся в источнике мультимедиа. Любые другие типы потоков, например потоки данных, игнорируются.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'Метод Имедиадет:: get_OutputStreams (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679710"
---
# <a name="imediadetget_outputstreams-method"></a><span data-ttu-id="ae6f3-104">Метод Имедиадет:: Get \_ аутпутстреамс</span><span class="sxs-lookup"><span data-stu-id="ae6f3-104">IMediaDet::get\_OutputStreams method</span></span>

> [!Note]  
> <span data-ttu-id="ae6f3-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ae6f3-105">\[Deprecated.</span></span> <span data-ttu-id="ae6f3-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae6f3-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ae6f3-107">`get_OutputStreams`Метод извлекает количество аудио и видеопотоков, содержащихся в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ae6f3-107">The `get_OutputStreams` method retrieves the number of audio and video streams contained in the media source.</span></span> <span data-ttu-id="ae6f3-108">Любые другие типы потоков, например потоки данных, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ae6f3-108">Any other stream types, such as data streams, are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6f3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae6f3-109">Syntax</span></span>


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ae6f3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae6f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae6f3-111">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ae6f3-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ae6f3-112">Получает число потоков вывода.</span><span class="sxs-lookup"><span data-stu-id="ae6f3-112">Receives the number of output streams.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae6f3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae6f3-113">Return value</span></span>

<span data-ttu-id="ae6f3-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ae6f3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae6f3-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae6f3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae6f3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae6f3-116">Remarks</span></span>

<span data-ttu-id="ae6f3-117">Перед вызовом этого метода вызовите [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) , чтобы задать имя файла.</span><span class="sxs-lookup"><span data-stu-id="ae6f3-117">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="ae6f3-118">Если средство обнаружения мультимедиа находится в режиме захвата растрового изображения, этот метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="ae6f3-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="ae6f3-119">Дополнительные сведения см. в разделе [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="ae6f3-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="ae6f3-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ae6f3-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ae6f3-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae6f3-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ae6f3-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ae6f3-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae6f3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ae6f3-123">Requirements</span></span>



| <span data-ttu-id="ae6f3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ae6f3-124">Requirement</span></span> | <span data-ttu-id="ae6f3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ae6f3-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6f3-126">Header</span><span class="sxs-lookup"><span data-stu-id="ae6f3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ae6f3-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae6f3-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ae6f3-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae6f3-128">Library</span></span><br/> | <dl> <span data-ttu-id="ae6f3-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae6f3-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae6f3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae6f3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6f3-131">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="ae6f3-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="ae6f3-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ae6f3-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




