---
description: 'Метод Жетдефаулттранситионб извлекает переход по умолчанию. Этот метод эквивалентен Иамтимелине:: Жетдефаулттранситион, но получает значение BSTR, а не GUID.'
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: 'Метод Иамтимелине:: Жетдефаулттранситионб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f150ca0fafff6b250776a38b7ec68beb470e9d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679870"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a><span data-ttu-id="5e0fc-104">Метод Иамтимелине:: Жетдефаулттранситионб</span><span class="sxs-lookup"><span data-stu-id="5e0fc-104">IAMTimeline::GetDefaultTransitionB method</span></span>

> [!Note]  
> <span data-ttu-id="5e0fc-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5e0fc-105">\[Deprecated.</span></span> <span data-ttu-id="5e0fc-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5e0fc-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5e0fc-107">`GetDefaultTransitionB`Метод получает переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e0fc-107">The `GetDefaultTransitionB` method retrieves the default transition.</span></span> <span data-ttu-id="5e0fc-108">Этот метод эквивалентен [**иамтимелине:: жетдефаулттранситион**](iamtimeline-getdefaulttransition.md), но получает значение BSTR, а не GUID.</span><span class="sxs-lookup"><span data-stu-id="5e0fc-108">This method is equivalent to [**IAMTimeline::GetDefaultTransition**](iamtimeline-getdefaulttransition.md), but receives a BSTR value, rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e0fc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e0fc-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="5e0fc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e0fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e0fc-111">*пгуид* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5e0fc-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0fc-112">Получает значение **BSTR** , ПРЕДСТАВЛЯЮЩЕЕ идентификатор GUID перехода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e0fc-112">Receives a **BSTR** value representing the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e0fc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e0fc-113">Return value</span></span>

<span data-ttu-id="5e0fc-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e0fc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e0fc-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e0fc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e0fc-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e0fc-116">Remarks</span></span>

<span data-ttu-id="5e0fc-117">Метод выделяет память для строки.</span><span class="sxs-lookup"><span data-stu-id="5e0fc-117">The method allocates memory for the string.</span></span> <span data-ttu-id="5e0fc-118">Приложение должно вызвать **сисфристринг** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="5e0fc-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="5e0fc-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5e0fc-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5e0fc-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e0fc-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5e0fc-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5e0fc-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e0fc-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5e0fc-122">Requirements</span></span>



| <span data-ttu-id="5e0fc-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5e0fc-123">Requirement</span></span> | <span data-ttu-id="5e0fc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5e0fc-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e0fc-125">Header</span><span class="sxs-lookup"><span data-stu-id="5e0fc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5e0fc-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e0fc-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5e0fc-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e0fc-127">Library</span></span><br/> | <dl> <span data-ttu-id="5e0fc-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e0fc-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e0fc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e0fc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e0fc-130">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="5e0fc-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="5e0fc-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5e0fc-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




