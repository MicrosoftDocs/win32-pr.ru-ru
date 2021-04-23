---
description: Метод Сетлоккед устанавливает состояние редактирования объекта как "заблокировано" или "Разблокировано".
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'Метод Иамтимелинеобж:: Сетлоккед (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676041"
---
# <a name="iamtimelineobjsetlocked-method"></a><span data-ttu-id="5ad4d-103">Метод Иамтимелинеобж:: Сетлоккед</span><span class="sxs-lookup"><span data-stu-id="5ad4d-103">IAMTimelineObj::SetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="5ad4d-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-104">\[Deprecated.</span></span> <span data-ttu-id="5ad4d-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5ad4d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5ad4d-106">`SetLocked`Метод устанавливает состояние редактирования объекта как "заблокировано" или "Разблокировано".</span><span class="sxs-lookup"><span data-stu-id="5ad4d-106">The `SetLocked` method sets the object's editing state to locked or unlocked.</span></span>

<span data-ttu-id="5ad4d-107">Заблокированное состояние указывает, что объект не должен редактироваться; незаблокированное состояние указывает, что объект можно изменять.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="5ad4d-108">Временная шкала не обеспечивает принудительную блокировку.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="5ad4d-109">Параметр блокировки существует только для удобства приложения.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad4d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ad4d-110">Syntax</span></span>


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="5ad4d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ad4d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad4d-112">*неввал*</span><span class="sxs-lookup"><span data-stu-id="5ad4d-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad4d-113">Логическое значение, указывающее состояние редактирования объекта.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-113">Boolean value that specifies the object's editing state.</span></span> <span data-ttu-id="5ad4d-114">Если **значение — true**, объект заблокирован и не должен редактироваться.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-114">If **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="5ad4d-115">Если **значение равно false**, объект разблокируется и может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ad4d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ad4d-116">Return value</span></span>

<span data-ttu-id="5ad4d-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ad4d-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ad4d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ad4d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ad4d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ad4d-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5ad4d-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ad4d-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ad4d-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5ad4d-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5ad4d-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ad4d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5ad4d-123">Requirements</span></span>



| <span data-ttu-id="5ad4d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5ad4d-124">Requirement</span></span> | <span data-ttu-id="5ad4d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5ad4d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad4d-126">Header</span><span class="sxs-lookup"><span data-stu-id="5ad4d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5ad4d-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4d-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5ad4d-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ad4d-128">Library</span></span><br/> | <dl> <span data-ttu-id="5ad4d-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4d-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad4d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ad4d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad4d-131">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="5ad4d-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5ad4d-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5ad4d-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




