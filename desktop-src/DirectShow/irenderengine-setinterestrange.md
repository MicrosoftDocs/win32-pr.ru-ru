---
description: 'Метод Ирендеренгине:: Сетинтерестранже не поддерживается.'
ms.assetid: 1e4c3bd4-2540-428f-9ca6-dd4c65c53434
title: 'Метод Ирендеренгине:: Сетинтерестранже'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetInterestRange
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec9790e65efa30b83cf324da4153f20c541733b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084462"
---
# <a name="irenderenginesetinterestrange-method"></a><span data-ttu-id="b322b-103">Метод Ирендеренгине:: Сетинтерестранже</span><span class="sxs-lookup"><span data-stu-id="b322b-103">IRenderEngine::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="b322b-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b322b-104">\[Deprecated.</span></span> <span data-ttu-id="b322b-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b322b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b322b-106">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b322b-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="b322b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b322b-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="b322b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b322b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b322b-109">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="b322b-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="b322b-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="b322b-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b322b-111">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="b322b-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="b322b-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="b322b-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b322b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b322b-113">Return value</span></span>

<span data-ttu-id="b322b-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b322b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b322b-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b322b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b322b-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="b322b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b322b-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="b322b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b322b-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b322b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b322b-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b322b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="b322b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="b322b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b322b-121">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="b322b-121">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> </dl>

 

 



