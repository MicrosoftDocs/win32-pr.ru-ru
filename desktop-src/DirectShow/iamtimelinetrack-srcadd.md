---
description: Метод Сркадд добавляет источник к дорожке.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'Метод Иамтимелинетракк:: Сркадд (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685228"
---
# <a name="iamtimelinetracksrcadd-method"></a><span data-ttu-id="de0b1-103">Метод Иамтимелинетракк:: Сркадд</span><span class="sxs-lookup"><span data-stu-id="de0b1-103">IAMTimelineTrack::SrcAdd method</span></span>

> [!Note]  
> <span data-ttu-id="de0b1-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="de0b1-104">\[Deprecated.</span></span> <span data-ttu-id="de0b1-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de0b1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="de0b1-106">`SrcAdd`Метод добавляет источник к дорожке.</span><span class="sxs-lookup"><span data-stu-id="de0b1-106">The `SrcAdd` method adds a source to the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="de0b1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de0b1-107">Syntax</span></span>


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="de0b1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="de0b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de0b1-109">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="de0b1-109">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="de0b1-110">Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="de0b1-110">Pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de0b1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de0b1-111">Return value</span></span>

<span data-ttu-id="de0b1-112">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="de0b1-112">Returns S\_OK if successful.</span></span> <span data-ttu-id="de0b1-113">Возвращает E \_ Interface, если объект не является исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="de0b1-113">Returns E\_NOINTERFACE if the object is not a source object.</span></span> <span data-ttu-id="de0b1-114">В противном случае возвращает значение **HRESULT** , указывающее причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="de0b1-114">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="de0b1-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de0b1-115">Remarks</span></span>

<span data-ttu-id="de0b1-116">Задайте время начала и окончания работы источника перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="de0b1-116">Set the source's start and stop times before calling this method.</span></span> <span data-ttu-id="de0b1-117">(Вызовите [**иамтимелинеобж:: сетстартстоп**](iamtimelineobj-setstartstop.md).)</span><span class="sxs-lookup"><span data-stu-id="de0b1-117">(Call [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md).)</span></span>

<span data-ttu-id="de0b1-118">В настоящее время DES не может одновременно визуализировать более 75 источников, которые были сжаты с помощью кодеков для сжатия видео (ВКМ).</span><span class="sxs-lookup"><span data-stu-id="de0b1-118">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="de0b1-119">Кроме того, если проект в целом содержит более 75 таких источников, необходимо использовать динамическое переподключение или DES не может выполнить предварительный просмотр проекта.</span><span class="sxs-lookup"><span data-stu-id="de0b1-119">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="de0b1-120">Дополнительные сведения см. в разделе [**ирендеренгине:: сетдинамикреконнектлевел**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="de0b1-120">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="de0b1-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="de0b1-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="de0b1-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="de0b1-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="de0b1-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="de0b1-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de0b1-124">Требования</span><span class="sxs-lookup"><span data-stu-id="de0b1-124">Requirements</span></span>



| <span data-ttu-id="de0b1-125">Требование</span><span class="sxs-lookup"><span data-stu-id="de0b1-125">Requirement</span></span> | <span data-ttu-id="de0b1-126">Значение</span><span class="sxs-lookup"><span data-stu-id="de0b1-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de0b1-127">Header</span><span class="sxs-lookup"><span data-stu-id="de0b1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="de0b1-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="de0b1-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="de0b1-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="de0b1-129">Library</span></span><br/> | <dl> <span data-ttu-id="de0b1-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de0b1-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0b1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de0b1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0b1-132">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="de0b1-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="de0b1-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="de0b1-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




