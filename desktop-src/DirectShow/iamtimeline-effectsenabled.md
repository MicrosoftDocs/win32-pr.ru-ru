---
description: Метод Еффектсенаблед определяет, включены ли эффекты. Если эффекты отключены, они остаются на временной шкале, но не подготавливаются к просмотру.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: 'Метод Иамтимелине:: Еффектсенаблед (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d988e8a4c10dc6dba52269c6729b8d7fea1f090e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651789"
---
# <a name="iamtimelineeffectsenabled-method"></a><span data-ttu-id="88c35-104">Метод Иамтимелине:: Еффектсенаблед</span><span class="sxs-lookup"><span data-stu-id="88c35-104">IAMTimeline::EffectsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="88c35-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="88c35-105">\[Deprecated.</span></span> <span data-ttu-id="88c35-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="88c35-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="88c35-107">`EffectsEnabled`Метод определяет, включены ли эффекты.</span><span class="sxs-lookup"><span data-stu-id="88c35-107">The `EffectsEnabled` method determines whether effects are enabled.</span></span> <span data-ttu-id="88c35-108">Если эффекты отключены, они остаются на временной шкале, но не подготавливаются к просмотру.</span><span class="sxs-lookup"><span data-stu-id="88c35-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c35-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88c35-109">Syntax</span></span>


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="88c35-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="88c35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88c35-111">*пфенаблед*</span><span class="sxs-lookup"><span data-stu-id="88c35-111">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="88c35-112">Получает логическое значение, указывающее, включены ли эффекты.</span><span class="sxs-lookup"><span data-stu-id="88c35-112">Receives a Boolean value indicating whether effects are enabled.</span></span> <span data-ttu-id="88c35-113">Если **значение равно true**, эффекты включены.</span><span class="sxs-lookup"><span data-stu-id="88c35-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="88c35-114">Если задано **значение false**, эффекты отключены.</span><span class="sxs-lookup"><span data-stu-id="88c35-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88c35-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88c35-115">Return value</span></span>

<span data-ttu-id="88c35-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="88c35-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88c35-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88c35-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88c35-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88c35-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="88c35-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="88c35-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="88c35-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="88c35-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="88c35-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="88c35-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88c35-122">Требования</span><span class="sxs-lookup"><span data-stu-id="88c35-122">Requirements</span></span>



| <span data-ttu-id="88c35-123">Требование</span><span class="sxs-lookup"><span data-stu-id="88c35-123">Requirement</span></span> | <span data-ttu-id="88c35-124">Значение</span><span class="sxs-lookup"><span data-stu-id="88c35-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88c35-125">Header</span><span class="sxs-lookup"><span data-stu-id="88c35-125">Header</span></span><br/>  | <dl> <span data-ttu-id="88c35-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c35-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="88c35-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88c35-127">Library</span></span><br/> | <dl> <span data-ttu-id="88c35-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88c35-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88c35-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88c35-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c35-130">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="88c35-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="88c35-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="88c35-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




