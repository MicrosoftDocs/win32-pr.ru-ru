---
description: Метод Жетграупкомпрессор извлекает фильтр сжатия для указанной группы.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'Метод Исмартрендеренгине:: Жетграупкомпрессор (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675614"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a><span data-ttu-id="f98ea-103">Метод Исмартрендеренгине:: Жетграупкомпрессор</span><span class="sxs-lookup"><span data-stu-id="f98ea-103">ISmartRenderEngine::GetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="f98ea-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f98ea-104">\[Deprecated.</span></span> <span data-ttu-id="f98ea-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f98ea-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f98ea-106">`GetGroupCompressor`Метод извлекает фильтр сжатия для указанной группы.</span><span class="sxs-lookup"><span data-stu-id="f98ea-106">The `GetGroupCompressor` method retrieves the compression filter for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98ea-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f98ea-107">Syntax</span></span>


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="f98ea-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f98ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f98ea-109">*Группа*</span><span class="sxs-lookup"><span data-stu-id="f98ea-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="f98ea-110">Отсчитываемый от нуля индекс группы.</span><span class="sxs-lookup"><span data-stu-id="f98ea-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="f98ea-111">*пкомпрессор*</span><span class="sxs-lookup"><span data-stu-id="f98ea-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="f98ea-112">Получает указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра сжатия.</span><span class="sxs-lookup"><span data-stu-id="f98ea-112">Receives a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span> <span data-ttu-id="f98ea-113">Если фильтр сжатия отсутствует, он получает значение **null** .</span><span class="sxs-lookup"><span data-stu-id="f98ea-113">It receives the value **NULL** if there is no compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f98ea-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f98ea-114">Return value</span></span>

<span data-ttu-id="f98ea-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f98ea-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f98ea-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f98ea-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f98ea-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f98ea-117">Remarks</span></span>

<span data-ttu-id="f98ea-118">Этот метод используется для задания свойств фильтра сжатия, например частоты ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="f98ea-118">Use this method to set properties on the compression filter, such as the key-frame rate.</span></span> <span data-ttu-id="f98ea-119">Вызовите этот метод после вызова [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md), но перед отрисовкой проекта.</span><span class="sxs-lookup"><span data-stu-id="f98ea-119">Call this method after calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md), but before rendering the project.</span></span> <span data-ttu-id="f98ea-120">Затем запросите выходной ПИН-код фильтра сжатия для интерфейса [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , который содержит методы для настройки параметров сжатия.</span><span class="sxs-lookup"><span data-stu-id="f98ea-120">Then query the compression filter's output pin for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, which contains methods for setting compression parameters.</span></span> <span data-ttu-id="f98ea-121">Выпустите интерфейс по завершении.</span><span class="sxs-lookup"><span data-stu-id="f98ea-121">Release the interface when you are done.</span></span> <span data-ttu-id="f98ea-122">При внесении последующих изменений на временную шкалу вызовите **коннектфронтенд**, а затем снова вызовите **жетграупкомпрессор** , чтобы сбросить параметры сжатия.</span><span class="sxs-lookup"><span data-stu-id="f98ea-122">If you make any subsequent changes to the timeline, call **ConnectFrontEnd**, and then call **GetGroupCompressor** again to reset the compression parameters.</span></span>

<span data-ttu-id="f98ea-123">При возврате, если значение \* *Пкомпрессор* не **равно NULL**, то интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="f98ea-123">On return, if the value of \**pCompressor* is non-**NULL**, the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface has an outstanding reference count.</span></span> <span data-ttu-id="f98ea-124">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="f98ea-124">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="f98ea-125">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f98ea-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f98ea-126">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f98ea-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f98ea-127">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f98ea-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f98ea-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f98ea-128">Requirements</span></span>



| <span data-ttu-id="f98ea-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f98ea-129">Requirement</span></span> | <span data-ttu-id="f98ea-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f98ea-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f98ea-131">Header</span><span class="sxs-lookup"><span data-stu-id="f98ea-131">Header</span></span><br/>  | <dl> <span data-ttu-id="f98ea-132"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f98ea-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f98ea-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f98ea-133">Library</span></span><br/> | <dl> <span data-ttu-id="f98ea-134"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f98ea-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f98ea-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f98ea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98ea-136">**Интерфейс Исмартрендеренгине**</span><span class="sxs-lookup"><span data-stu-id="f98ea-136">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="f98ea-137">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f98ea-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




