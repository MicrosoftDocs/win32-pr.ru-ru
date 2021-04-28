---
description: 'Метод Иамтимелине:: Жетинсертмоде не поддерживается.'
ms.assetid: 864c2805-be19-4e25-acaa-9fd0466d788d
title: 'Метод Иамтимелине:: Жетинсертмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetInsertMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32f81ac0f068f7b0963193306bb0c84c3b1ba91f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098702"
---
# <a name="iamtimelinegetinsertmode-method"></a><span data-ttu-id="4d30f-103">Метод Иамтимелине:: Жетинсертмоде</span><span class="sxs-lookup"><span data-stu-id="4d30f-103">IAMTimeline::GetInsertMode method</span></span>

> [!Note]  
> <span data-ttu-id="4d30f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4d30f-104">\[Deprecated.</span></span> <span data-ttu-id="4d30f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d30f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4d30f-106">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4d30f-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d30f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d30f-107">Syntax</span></span>


```C++
HRESULT GetInsertMode(
   long *pMode
);
```



## <a name="parameters"></a><span data-ttu-id="4d30f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d30f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d30f-109">*пмоде*</span><span class="sxs-lookup"><span data-stu-id="4d30f-109">*pMode*</span></span> 
</dt> <dd>

<span data-ttu-id="4d30f-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4d30f-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d30f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d30f-111">Return value</span></span>

<span data-ttu-id="4d30f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4d30f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d30f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d30f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d30f-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="4d30f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4d30f-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4d30f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4d30f-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4d30f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4d30f-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4d30f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d30f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4d30f-118">Requirements</span></span>



| <span data-ttu-id="4d30f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4d30f-119">Requirement</span></span> | <span data-ttu-id="4d30f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4d30f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d30f-121">Header</span><span class="sxs-lookup"><span data-stu-id="4d30f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4d30f-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d30f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4d30f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4d30f-123">Library</span></span><br/> | <dl> <span data-ttu-id="4d30f-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d30f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d30f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4d30f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d30f-126">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="4d30f-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




