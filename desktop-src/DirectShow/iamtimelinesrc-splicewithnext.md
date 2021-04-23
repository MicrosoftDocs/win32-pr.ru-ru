---
description: Метод Сплицевиснекст соединяет исходный объект с другим исходным объектом.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'Метод Иамтимелинесрк:: Сплицевиснекст (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685195"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a><span data-ttu-id="5a39e-103">Метод Иамтимелинесрк:: Сплицевиснекст</span><span class="sxs-lookup"><span data-stu-id="5a39e-103">IAMTimelineSrc::SpliceWithNext method</span></span>

> [!Note]  
> <span data-ttu-id="5a39e-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5a39e-104">\[Deprecated.</span></span> <span data-ttu-id="5a39e-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a39e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a39e-106">`SpliceWithNext`Метод присоединяет исходный объект к другому исходному объекту.</span><span class="sxs-lookup"><span data-stu-id="5a39e-106">The `SpliceWithNext` method joins the source object to another source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a39e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a39e-107">Syntax</span></span>


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a><span data-ttu-id="5a39e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a39e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a39e-109">*пнекст*</span><span class="sxs-lookup"><span data-stu-id="5a39e-109">*pNext*</span></span> 
</dt> <dd>

<span data-ttu-id="5a39e-110">Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта, который необходимо присоединить к текущему источнику.</span><span class="sxs-lookup"><span data-stu-id="5a39e-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object to join to the current source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a39e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a39e-111">Return value</span></span>

<span data-ttu-id="5a39e-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a39e-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5a39e-113">Возможные возвращаемые значения включают следующее.</span><span class="sxs-lookup"><span data-stu-id="5a39e-113">Possible return values include the following:</span></span>



| <span data-ttu-id="5a39e-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5a39e-114">Return code</span></span>                                                                                   | <span data-ttu-id="5a39e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5a39e-115">Description</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a39e-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5a39e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5a39e-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5a39e-117">Success.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="5a39e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5a39e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5a39e-119">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="5a39e-119">Invalid argument.</span></span><br/>                                             |
| <dl> <span data-ttu-id="5a39e-120"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a39e-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="5a39e-121">Объект, указанный параметром *пнекст* , не является исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="5a39e-121">Object specified by *pNext* parameter is not a source object.</span></span><br/> |
| <dl> <span data-ttu-id="5a39e-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a39e-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5a39e-123">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="5a39e-123">**NULL** pointer argument.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="5a39e-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a39e-124">Remarks</span></span>

<span data-ttu-id="5a39e-125">Как уже реализовано, этот метод отклоняет любые эффекты в *пнекст*.</span><span class="sxs-lookup"><span data-stu-id="5a39e-125">As currently implemented, this method discards any effects on *pNext*.</span></span>

<span data-ttu-id="5a39e-126">Чтобы этот метод был выполнен, *пнекст* должен быть кадром соответствия текущего исходного объекта, который определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5a39e-126">For this method to succeed, *pNext* must be a match frame of the current source object, defined as follows:</span></span>

-   <span data-ttu-id="5a39e-127">Он должен использовать один и тот же исходный файл.</span><span class="sxs-lookup"><span data-stu-id="5a39e-127">It must share the same source file.</span></span>
-   <span data-ttu-id="5a39e-128">Время запуска носителя должно совпадать с временем окончания текущего источника.</span><span class="sxs-lookup"><span data-stu-id="5a39e-128">The media start time must equal the media stop time of the current source.</span></span>
-   <span data-ttu-id="5a39e-129">Скорость воспроизведения должна быть одинаковой.</span><span class="sxs-lookup"><span data-stu-id="5a39e-129">The playback rate must be the same.</span></span> <span data-ttu-id="5a39e-130">Скорость воспроизведения — длительность носителя, деленная на длительность временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="5a39e-130">Playback rate is media duration divided by timeline duration.</span></span>

> [!Note]  
> <span data-ttu-id="5a39e-131">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5a39e-131">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5a39e-132">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5a39e-132">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5a39e-133">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5a39e-133">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a39e-134">Требования</span><span class="sxs-lookup"><span data-stu-id="5a39e-134">Requirements</span></span>



| <span data-ttu-id="5a39e-135">Требование</span><span class="sxs-lookup"><span data-stu-id="5a39e-135">Requirement</span></span> | <span data-ttu-id="5a39e-136">Значение</span><span class="sxs-lookup"><span data-stu-id="5a39e-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a39e-137">Header</span><span class="sxs-lookup"><span data-stu-id="5a39e-137">Header</span></span><br/>  | <dl> <span data-ttu-id="5a39e-138"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a39e-138"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5a39e-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a39e-139">Library</span></span><br/> | <dl> <span data-ttu-id="5a39e-140"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a39e-140"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a39e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a39e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a39e-142">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="5a39e-142">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="5a39e-143">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5a39e-143">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




