---
description: Метод Жетрекурсивелайерофтипе выполняет упорядочение по глубине виртуальных дорожек, содержащихся в этой композиции, и получает n-го виртуального дорожки из этого порядка.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'Метод Иамтимелинекомп:: Жетрекурсивелайерофтипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679788"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a><span data-ttu-id="83bfe-103">Метод Иамтимелинекомп:: Жетрекурсивелайерофтипе</span><span class="sxs-lookup"><span data-stu-id="83bfe-103">IAMTimelineComp::GetRecursiveLayerOfType method</span></span>

> [!Note]  
> <span data-ttu-id="83bfe-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="83bfe-104">\[Deprecated.</span></span> <span data-ttu-id="83bfe-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="83bfe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="83bfe-106">`GetRecursiveLayerOfType`Метод выполняет упорядочение по глубине виртуальных дорожек, содержащихся в этой композиции, и извлекает из этого упорядочения *n*-й виртуальный объект Track.</span><span class="sxs-lookup"><span data-stu-id="83bfe-106">The `GetRecursiveLayerOfType` method performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span>

## <a name="syntax"></a><span data-ttu-id="83bfe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83bfe-107">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="83bfe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83bfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83bfe-109">*ппвиртуалтракк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="83bfe-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83bfe-110">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) виртуальной записи.</span><span class="sxs-lookup"><span data-stu-id="83bfe-110">Receives a pointer to the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="83bfe-111">*вхичлайер*</span><span class="sxs-lookup"><span data-stu-id="83bfe-111">*WhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="83bfe-112">Указывает, какую виртуальную дорожку следует получить, проиндексировать из нуля.</span><span class="sxs-lookup"><span data-stu-id="83bfe-112">Specifies which virtual track to retrieve, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="83bfe-113">*Тип*</span><span class="sxs-lookup"><span data-stu-id="83bfe-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="83bfe-114">Член перечислимого [**типа \_ \_ временной шкалы**](timeline-major-type.md) , указывающий, следует ли включать в поиск записи.</span><span class="sxs-lookup"><span data-stu-id="83bfe-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type that specifies whether to include tracks in the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83bfe-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83bfe-115">Return value</span></span>

<span data-ttu-id="83bfe-116">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="83bfe-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="83bfe-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="83bfe-117">Return code</span></span>                                                                                  | <span data-ttu-id="83bfe-118">Описание</span><span class="sxs-lookup"><span data-stu-id="83bfe-118">Description</span></span>                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="83bfe-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="83bfe-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="83bfe-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="83bfe-120">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="83bfe-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="83bfe-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="83bfe-122">Нет объекта указанного типа.</span><span class="sxs-lookup"><span data-stu-id="83bfe-122">No object of the specified type.</span></span><br/> |
| <dl> <span data-ttu-id="83bfe-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="83bfe-123"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="83bfe-124">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="83bfe-124">**NULL** pointer argument.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="83bfe-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83bfe-125">Remarks</span></span>

<span data-ttu-id="83bfe-126">Как правило, приложению не требуется вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="83bfe-126">Typically, an application will not need to call this method.</span></span>

<span data-ttu-id="83bfe-127">Если параметр *типа* относится к \_ ОСНОВНОМУ типу временной шкалы \_ \_ , то упорядочение по глубине включает в себя дорожки.</span><span class="sxs-lookup"><span data-stu-id="83bfe-127">If the *Type* parameter is TIMELINE\_MAJOR\_TYPE\_TRACK, the depth-first ordering includes tracks.</span></span> <span data-ttu-id="83bfe-128">В противном случае он включает только композиции и группы.</span><span class="sxs-lookup"><span data-stu-id="83bfe-128">If not, it includes only compositions and groups.</span></span> <span data-ttu-id="83bfe-129">Сам объект включается в упорядочение.</span><span class="sxs-lookup"><span data-stu-id="83bfe-129">The object itself is included in the ordering.</span></span>

<span data-ttu-id="83bfe-130">Например, в следующем расположении, начиная с композиции а, упорядочение будет иметь вид B, C, F, D, E, A.</span><span class="sxs-lookup"><span data-stu-id="83bfe-130">For example, in the following arrangement, starting from Composition A, the ordering would be B, C, F, D, E, A.</span></span>

![жетрекурсивелайерофтипе](images/composition.png)

<span data-ttu-id="83bfe-132">Если метод завершается успешно, интерфейс **иамтимелинеобж** , который он возвращает, имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="83bfe-132">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="83bfe-133">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="83bfe-133">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="83bfe-134">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="83bfe-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="83bfe-135">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="83bfe-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="83bfe-136">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="83bfe-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="83bfe-137">Требования</span><span class="sxs-lookup"><span data-stu-id="83bfe-137">Requirements</span></span>



| <span data-ttu-id="83bfe-138">Требование</span><span class="sxs-lookup"><span data-stu-id="83bfe-138">Requirement</span></span> | <span data-ttu-id="83bfe-139">Значение</span><span class="sxs-lookup"><span data-stu-id="83bfe-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83bfe-140">Header</span><span class="sxs-lookup"><span data-stu-id="83bfe-140">Header</span></span><br/>  | <dl> <span data-ttu-id="83bfe-141"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="83bfe-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="83bfe-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83bfe-142">Library</span></span><br/> | <dl> <span data-ttu-id="83bfe-143"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83bfe-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83bfe-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83bfe-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83bfe-145">**Интерфейс Иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="83bfe-145">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="83bfe-146">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="83bfe-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




