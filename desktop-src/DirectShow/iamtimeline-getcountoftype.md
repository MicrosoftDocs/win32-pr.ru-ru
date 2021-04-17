---
description: Метод Жеткаунтофтипе извлекает количество объектов указанного типа, содержащихся в указанной группе и всех ее дочерних элементах.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'Метод Иамтимелине:: Жеткаунтофтипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651786"
---
# <a name="iamtimelinegetcountoftype-method"></a><span data-ttu-id="75e16-103">Метод Иамтимелине:: Жеткаунтофтипе</span><span class="sxs-lookup"><span data-stu-id="75e16-103">IAMTimeline::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="75e16-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="75e16-104">\[Deprecated.</span></span> <span data-ttu-id="75e16-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75e16-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="75e16-106">`GetCountOfType`Метод извлекает количество объектов указанного типа, содержащихся в указанной группе и всех ее дочерних элементах.</span><span class="sxs-lookup"><span data-stu-id="75e16-106">The `GetCountOfType` method retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e16-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75e16-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="75e16-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="75e16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75e16-109">*Группа*</span><span class="sxs-lookup"><span data-stu-id="75e16-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="75e16-110">Номер индекса группы, для которой необходимо получить число.</span><span class="sxs-lookup"><span data-stu-id="75e16-110">Index number of the group for which to retrieve the count.</span></span>

</dd> <dt>

<span data-ttu-id="75e16-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="75e16-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="75e16-112">Получает число объектов указанного типа, содержащихся в группе, и всех его виртуальных дорожек рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="75e16-112">Receives the number of objects of the specified type contained in the group and all of its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="75e16-113">*пвалвискомпс*</span><span class="sxs-lookup"><span data-stu-id="75e16-113">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="75e16-114">Получает счетчик, возвращенный в *Pval* , и число композиций, в которых выполняется поиск, включая это.</span><span class="sxs-lookup"><span data-stu-id="75e16-114">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="75e16-115">*мажортипе*</span><span class="sxs-lookup"><span data-stu-id="75e16-115">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="75e16-116">Элемент перечисляемого типа " [**\_ основной \_ тип временной шкалы**](timeline-major-type.md) ", указывающий тип объекта для подсчета.</span><span class="sxs-lookup"><span data-stu-id="75e16-116">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75e16-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75e16-117">Return value</span></span>

<span data-ttu-id="75e16-118">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75e16-118">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="75e16-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="75e16-119">Return code</span></span>                                                                                  | <span data-ttu-id="75e16-120">Описание</span><span class="sxs-lookup"><span data-stu-id="75e16-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="75e16-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="75e16-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="75e16-122">Успешно.</span><span class="sxs-lookup"><span data-stu-id="75e16-122">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="75e16-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="75e16-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="75e16-124">Недопустимый номер группы.</span><span class="sxs-lookup"><span data-stu-id="75e16-124">Invalid group number.</span></span><br/>      |
| <dl> <span data-ttu-id="75e16-125"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="75e16-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="75e16-126">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="75e16-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75e16-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75e16-127">Remarks</span></span>

<span data-ttu-id="75e16-128">Вызов этого метода эквивалентен вызову [**иамтимелинекомп:: жеткаунтофтипе**](iamtimelinecomp-getcountoftype.md) для указанной группы.</span><span class="sxs-lookup"><span data-stu-id="75e16-128">Calling this method is equivalent to calling [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) on the specified group.</span></span> <span data-ttu-id="75e16-129">Дополнительные сведения см. в разделе "Примечания" этого метода.</span><span class="sxs-lookup"><span data-stu-id="75e16-129">See the Remarks section of that method for more information.</span></span>

<span data-ttu-id="75e16-130">Как правило, приложение не будет вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="75e16-130">Typically, an application will not call this method.</span></span> <span data-ttu-id="75e16-131">Он вызывается модулем визуализации внутри.</span><span class="sxs-lookup"><span data-stu-id="75e16-131">It is called internally by the render engine.</span></span>

> [!Note]  
> <span data-ttu-id="75e16-132">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="75e16-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="75e16-133">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="75e16-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="75e16-134">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="75e16-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="75e16-135">Требования</span><span class="sxs-lookup"><span data-stu-id="75e16-135">Requirements</span></span>



| <span data-ttu-id="75e16-136">Требование</span><span class="sxs-lookup"><span data-stu-id="75e16-136">Requirement</span></span> | <span data-ttu-id="75e16-137">Значение</span><span class="sxs-lookup"><span data-stu-id="75e16-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75e16-138">Header</span><span class="sxs-lookup"><span data-stu-id="75e16-138">Header</span></span><br/>  | <dl> <span data-ttu-id="75e16-139"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="75e16-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="75e16-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="75e16-140">Library</span></span><br/> | <dl> <span data-ttu-id="75e16-141"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75e16-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e16-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75e16-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e16-143">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="75e16-143">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="75e16-144">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="75e16-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




