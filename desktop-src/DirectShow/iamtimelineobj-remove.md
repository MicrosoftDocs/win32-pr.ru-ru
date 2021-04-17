---
description: Метод reinsert удаляет этот объект из временной шкалы (включая подобъекты, но не дочерние элементы) для повторной вставки в других местах.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'Метод Иамтимелинеобж:: Remove (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689151"
---
# <a name="iamtimelineobjremove-method"></a><span data-ttu-id="7db65-103">Метод Иамтимелинеобж:: Remove</span><span class="sxs-lookup"><span data-stu-id="7db65-103">IAMTimelineObj::Remove method</span></span>

> [!Note]  
> <span data-ttu-id="7db65-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7db65-104">\[Deprecated.</span></span> <span data-ttu-id="7db65-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7db65-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7db65-106">`Remove`Метод удаляет этот объект из временной шкалы (включая подобъекты, но не дочерние элементы) для повторной вставки в других местах.</span><span class="sxs-lookup"><span data-stu-id="7db65-106">The `Remove` method removes this object from the timeline (including subobjects but not children), for reinsertion elsewhere.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db65-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7db65-107">Syntax</span></span>


```C++
HRESULT Remove();
```



## <a name="parameters"></a><span data-ttu-id="7db65-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7db65-108">Parameters</span></span>

<span data-ttu-id="7db65-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7db65-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7db65-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7db65-110">Return value</span></span>

<span data-ttu-id="7db65-111">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7db65-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7db65-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7db65-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7db65-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7db65-113">Remarks</span></span>

<span data-ttu-id="7db65-114">Этот метод следует вызывать только в том случае, если приложение немедленно вставит объект обратно на временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="7db65-114">Call this method only if the application will immediately insert the object back into the timeline.</span></span> <span data-ttu-id="7db65-115">Недопустимая операция для вызова этого метода без повторной вставки объекта.</span><span class="sxs-lookup"><span data-stu-id="7db65-115">It is an invalid operation to call this method without then reinserting the object.</span></span> <span data-ttu-id="7db65-116">Чтобы окончательно удалить объект, вызовите [**иамтимелинеобж:: RemoveAll**](iamtimelineobj-removeall.md).</span><span class="sxs-lookup"><span data-stu-id="7db65-116">To remove an object permanently, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).</span></span>

> [!Note]  
> <span data-ttu-id="7db65-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="7db65-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7db65-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7db65-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7db65-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7db65-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7db65-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7db65-120">Requirements</span></span>



| <span data-ttu-id="7db65-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7db65-121">Requirement</span></span> | <span data-ttu-id="7db65-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7db65-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7db65-123">Header</span><span class="sxs-lookup"><span data-stu-id="7db65-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7db65-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="7db65-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7db65-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7db65-125">Library</span></span><br/> | <dl> <span data-ttu-id="7db65-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7db65-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7db65-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7db65-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db65-128">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="7db65-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="7db65-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="7db65-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




