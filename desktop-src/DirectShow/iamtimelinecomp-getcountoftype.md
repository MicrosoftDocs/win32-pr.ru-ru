---
description: Метод Жеткаунтофтипе извлекает количество объектов заданного типа, содержащихся в этой композиции, и всех ее виртуальных дорожках, рекурсивно.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'Метод Иамтимелинекомп:: Жеткаунтофтипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679791"
---
# <a name="iamtimelinecompgetcountoftype-method"></a><span data-ttu-id="0e253-103">Метод Иамтимелинекомп:: Жеткаунтофтипе</span><span class="sxs-lookup"><span data-stu-id="0e253-103">IAMTimelineComp::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="0e253-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0e253-104">\[Deprecated.</span></span> <span data-ttu-id="0e253-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e253-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e253-106">`GetCountOfType`Метод извлекает количество объектов заданного типа, содержащихся в этой композиции, и всех виртуальных дорожках, рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="0e253-106">The `GetCountOfType` method retrieves the number of objects of a given type contained in this composition and all its virtual tracks, recursively.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e253-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e253-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="0e253-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e253-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e253-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="0e253-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0e253-110">Получает число объектов указанного типа, содержащихся в этой композиции и всех виртуальных дорожках, рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="0e253-110">Receives the number of objects of the specified type contained in this composition and all its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="0e253-111">*пвалвискомпс*</span><span class="sxs-lookup"><span data-stu-id="0e253-111">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="0e253-112">Получает счетчик, возвращенный в *Pval* , и число композиций, в которых выполняется поиск, включая это.</span><span class="sxs-lookup"><span data-stu-id="0e253-112">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="0e253-113">*мажортипе*</span><span class="sxs-lookup"><span data-stu-id="0e253-113">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="0e253-114">Элемент перечисляемого типа " [**\_ основной \_ тип временной шкалы**](timeline-major-type.md) ", указывающий тип объекта для подсчета.</span><span class="sxs-lookup"><span data-stu-id="0e253-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e253-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e253-115">Return value</span></span>

<span data-ttu-id="0e253-116">Возвращает \_ значение ОК, если успешно, или \_ указатель E в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0e253-116">Returns S\_OK if successful, or E\_POINTER otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e253-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e253-117">Remarks</span></span>

<span data-ttu-id="0e253-118">Как правило, приложение не будет вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="0e253-118">Typically, an application will not call this method.</span></span> <span data-ttu-id="0e253-119">Он вызывается модулем визуализации.</span><span class="sxs-lookup"><span data-stu-id="0e253-119">It is called by the render engine.</span></span>

<span data-ttu-id="0e253-120">При подсчете композиций значение, возвращаемое в *Pval* , равно нулю, а значение, возвращаемое в *пвалвискомпс* , — число композиций.</span><span class="sxs-lookup"><span data-stu-id="0e253-120">If you count compositions, the value returned in *pVal* is zero and the value returned in *pValWithComps* is the number of compositions.</span></span> <span data-ttu-id="0e253-121">Значение *\* пвалвискомпс* включает композицию, для которой вызывается метод.</span><span class="sxs-lookup"><span data-stu-id="0e253-121">The value of *\*pValWithComps* includes the composition on which you call the method.</span></span> <span data-ttu-id="0e253-122">Например, при вызове этого метода для пустой композиции *\* пвалвискомпс* равно 1.</span><span class="sxs-lookup"><span data-stu-id="0e253-122">For example, if you call this method on an empty composition, *\*pValWithComps* equals 1.</span></span>

<span data-ttu-id="0e253-123">Группы не могут находиться внутри композиций, поэтому этот метод нельзя использовать для подсчета групп.</span><span class="sxs-lookup"><span data-stu-id="0e253-123">Groups cannot reside inside compositions, so you cannot use this method to count groups.</span></span> <span data-ttu-id="0e253-124">(Возвращенное число всегда будет равно нулю.) Для подсчета групп вызовите метод [**иамтимелине:: жетграупкаунт**](iamtimeline-getgroupcount.md) .</span><span class="sxs-lookup"><span data-stu-id="0e253-124">(The returned count will always be zero.) To count groups, call the [**IAMTimeline::GetGroupCount**](iamtimeline-getgroupcount.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="0e253-125">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="0e253-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e253-126">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0e253-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0e253-127">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0e253-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e253-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0e253-128">Requirements</span></span>



| <span data-ttu-id="0e253-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0e253-129">Requirement</span></span> | <span data-ttu-id="0e253-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0e253-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e253-131">Header</span><span class="sxs-lookup"><span data-stu-id="0e253-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0e253-132"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e253-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0e253-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e253-133">Library</span></span><br/> | <dl> <span data-ttu-id="0e253-134"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e253-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e253-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e253-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e253-136">**Интерфейс Иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="0e253-136">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="0e253-137">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="0e253-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




