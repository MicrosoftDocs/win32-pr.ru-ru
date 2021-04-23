---
description: Задает фильтр сжатия, используемый при подготовке к просмотру указанной группы.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'Метод Исмартрендеренгине:: Сетграупкомпрессор (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680002"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a><span data-ttu-id="8b171-103">Метод Исмартрендеренгине:: Сетграупкомпрессор</span><span class="sxs-lookup"><span data-stu-id="8b171-103">ISmartRenderEngine::SetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="8b171-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8b171-104">\[Deprecated.</span></span> <span data-ttu-id="8b171-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b171-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8b171-106">Задает фильтр сжатия, используемый при подготовке к просмотру указанной группы.</span><span class="sxs-lookup"><span data-stu-id="8b171-106">Specifies a compression filter to use when rendering the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b171-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b171-107">Syntax</span></span>


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="8b171-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b171-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b171-109">*Группа*</span><span class="sxs-lookup"><span data-stu-id="8b171-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="8b171-110">Отсчитываемый от нуля индекс группы.</span><span class="sxs-lookup"><span data-stu-id="8b171-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="8b171-111">*пкомпрессор*</span><span class="sxs-lookup"><span data-stu-id="8b171-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="8b171-112">Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра сжатия.</span><span class="sxs-lookup"><span data-stu-id="8b171-112">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b171-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b171-113">Return value</span></span>

<span data-ttu-id="8b171-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8b171-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b171-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b171-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b171-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b171-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b171-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="8b171-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8b171-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8b171-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8b171-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8b171-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b171-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8b171-120">Requirements</span></span>



| <span data-ttu-id="8b171-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8b171-121">Requirement</span></span> | <span data-ttu-id="8b171-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8b171-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b171-123">Header</span><span class="sxs-lookup"><span data-stu-id="8b171-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8b171-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b171-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8b171-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b171-125">Library</span></span><br/> | <dl> <span data-ttu-id="8b171-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b171-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b171-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b171-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b171-128">**Интерфейс Исмартрендеренгине**</span><span class="sxs-lookup"><span data-stu-id="8b171-128">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="8b171-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="8b171-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




