---
description: Метод Иссмартрекомпрессформатсет определяет, был ли задан для группы формат смарт-сжатия.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'Метод Иамтимелинеграуп:: Иссмартрекомпрессформатсет (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675616"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a><span data-ttu-id="d3067-103">Метод Иамтимелинеграуп:: Иссмартрекомпрессформатсет</span><span class="sxs-lookup"><span data-stu-id="d3067-103">IAMTimelineGroup::IsSmartRecompressFormatSet method</span></span>

> [!Note]  
> <span data-ttu-id="d3067-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d3067-104">\[Deprecated.</span></span> <span data-ttu-id="d3067-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d3067-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d3067-106">`IsSmartRecompressFormatSet`Метод определяет, был ли задан формат смарт-сжатия для группы.</span><span class="sxs-lookup"><span data-stu-id="d3067-106">The `IsSmartRecompressFormatSet` method determines whether a smart recompression format was set for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3067-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3067-107">Syntax</span></span>


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d3067-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3067-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3067-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="d3067-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d3067-110">Получает логическое значение, указывающее, задан ли формат сжатия.</span><span class="sxs-lookup"><span data-stu-id="d3067-110">Receives a Boolean value indicating whether a compression format was set.</span></span> <span data-ttu-id="d3067-111">**Значение true** показывает, что был задан формат сжатия.</span><span class="sxs-lookup"><span data-stu-id="d3067-111">If **TRUE**, a compression format was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3067-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3067-112">Return value</span></span>

<span data-ttu-id="d3067-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3067-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3067-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3067-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3067-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3067-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d3067-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d3067-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d3067-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d3067-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d3067-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d3067-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3067-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d3067-119">Requirements</span></span>



| <span data-ttu-id="d3067-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d3067-120">Requirement</span></span> | <span data-ttu-id="d3067-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d3067-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3067-122">Header</span><span class="sxs-lookup"><span data-stu-id="d3067-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d3067-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3067-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d3067-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3067-124">Library</span></span><br/> | <dl> <span data-ttu-id="d3067-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3067-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3067-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3067-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3067-127">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="d3067-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="d3067-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d3067-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




