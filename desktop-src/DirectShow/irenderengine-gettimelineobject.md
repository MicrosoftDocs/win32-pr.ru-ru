---
description: Метод Жеттимелинеобжект извлекает временную шкалу, используемую подсистемой рендеринга в данный момент.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'Метод Ирендеренгине:: Жеттимелинеобжект (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676032"
---
# <a name="irenderenginegettimelineobject-method"></a><span data-ttu-id="ab83c-103">Метод Ирендеренгине:: Жеттимелинеобжект</span><span class="sxs-lookup"><span data-stu-id="ab83c-103">IRenderEngine::GetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="ab83c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ab83c-104">\[Deprecated.</span></span> <span data-ttu-id="ab83c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ab83c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ab83c-106">`GetTimelineObject`Метод получает временную шкалу, используемую в настоящий момент подсистемой отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ab83c-106">The `GetTimelineObject` method retrieves the timeline that the render engine is currently using.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab83c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab83c-107">Syntax</span></span>


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="ab83c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab83c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab83c-109">*пптимелине* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ab83c-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab83c-110">Получает указатель на интерфейс [**иамтимелине**](iamtimeline.md) временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="ab83c-110">Receives a pointer to the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="ab83c-111">Если шкала времени отсутствует, она получает значение **null** .</span><span class="sxs-lookup"><span data-stu-id="ab83c-111">It receives the value **NULL** if there is no timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab83c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab83c-112">Return value</span></span>

<span data-ttu-id="ab83c-113">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="ab83c-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ab83c-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ab83c-114">Return code</span></span>                                                                                            | <span data-ttu-id="ab83c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ab83c-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ab83c-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ab83c-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="ab83c-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ab83c-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="ab83c-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ab83c-118"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="ab83c-119">Недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="ab83c-119">Invalid pointer.</span></span><br/>                    |
| <dl> <span data-ttu-id="ab83c-120"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="ab83c-120"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="ab83c-121">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="ab83c-121">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab83c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab83c-122">Remarks</span></span>

<span data-ttu-id="ab83c-123">При возврате, если значение *\* Пптимелине* не **равно NULL**, то интерфейс **иамтимелине** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="ab83c-123">On return, if the value of *\*ppTimeline* is non-**NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="ab83c-124">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="ab83c-124">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="ab83c-125">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ab83c-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ab83c-126">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ab83c-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ab83c-127">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ab83c-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ab83c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ab83c-128">Requirements</span></span>



| <span data-ttu-id="ab83c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ab83c-129">Requirement</span></span> | <span data-ttu-id="ab83c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ab83c-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab83c-131">Header</span><span class="sxs-lookup"><span data-stu-id="ab83c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ab83c-132"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab83c-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ab83c-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ab83c-133">Library</span></span><br/> | <dl> <span data-ttu-id="ab83c-134"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab83c-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab83c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab83c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab83c-136">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="ab83c-136">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="ab83c-137">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ab83c-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




