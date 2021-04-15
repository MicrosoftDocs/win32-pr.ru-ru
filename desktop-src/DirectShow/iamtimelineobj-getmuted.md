---
description: Метод без звука Извлекает состояние отключения объекта.
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: 'Метод Иамтимелинеобж:: onвыкл. (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8883b03f9070a017b8fa4788a7cfd795f46c5f3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689182"
---
# <a name="iamtimelineobjgetmuted-method"></a><span data-ttu-id="73fb8-103">Метод Иамтимелинеобж:: onвыкл.</span><span class="sxs-lookup"><span data-stu-id="73fb8-103">IAMTimelineObj::GetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="73fb8-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="73fb8-104">\[Deprecated.</span></span> <span data-ttu-id="73fb8-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="73fb8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="73fb8-106">`GetMuted`Метод извлекает состояние отключения объекта.</span><span class="sxs-lookup"><span data-stu-id="73fb8-106">The `GetMuted` method retrieves the object's muted state.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fb8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73fb8-107">Syntax</span></span>


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="73fb8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="73fb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fb8-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="73fb8-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="73fb8-110">Получает значение, указывающее на выключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="73fb8-110">Receives a value indicating the muted state.</span></span> <span data-ttu-id="73fb8-111">Если значение равно **true**, то объект и его дочерние элементы будут отключены.</span><span class="sxs-lookup"><span data-stu-id="73fb8-111">If the value is **TRUE**, the object and its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fb8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73fb8-112">Return value</span></span>

<span data-ttu-id="73fb8-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="73fb8-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73fb8-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73fb8-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73fb8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73fb8-115">Remarks</span></span>

<span data-ttu-id="73fb8-116">Если родительский объект объекта отключен, то объект будет отключен независимо от состояния выключения.</span><span class="sxs-lookup"><span data-stu-id="73fb8-116">If an object's parent is muted, the object is muted regardless of its muted state.</span></span> <span data-ttu-id="73fb8-117">Если родительский элемент больше не выключен, восстанавливается предыдущее состояние звука объекта.</span><span class="sxs-lookup"><span data-stu-id="73fb8-117">When the parent is no longer muted, the object's previous muted state is restored.</span></span>

> [!Note]  
> <span data-ttu-id="73fb8-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="73fb8-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="73fb8-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="73fb8-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="73fb8-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="73fb8-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73fb8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="73fb8-121">Requirements</span></span>



| <span data-ttu-id="73fb8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="73fb8-122">Requirement</span></span> | <span data-ttu-id="73fb8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="73fb8-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73fb8-124">Header</span><span class="sxs-lookup"><span data-stu-id="73fb8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="73fb8-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="73fb8-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="73fb8-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73fb8-126">Library</span></span><br/> | <dl> <span data-ttu-id="73fb8-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73fb8-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73fb8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73fb8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fb8-129">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="73fb8-129">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="73fb8-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="73fb8-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




