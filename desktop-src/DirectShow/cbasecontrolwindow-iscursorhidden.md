---
description: Метод Искурсорхидден извлекает текущее состояние \_ элемента данных m бкурсорхидден.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Кбасеконтролвиндов. Искурсорхидден, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658109"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a><span data-ttu-id="df8aa-103">Кбасеконтролвиндов. Искурсорхидден, метод</span><span class="sxs-lookup"><span data-stu-id="df8aa-103">CBaseControlWindow.IsCursorHidden method</span></span>

<span data-ttu-id="df8aa-104">`IsCursorHidden`Метод получает текущее состояние элемента данных **m \_ бкурсорхидден** .</span><span class="sxs-lookup"><span data-stu-id="df8aa-104">The `IsCursorHidden` method retrieves the current state of the **m\_bCursorHidden** data member.</span></span>

## <a name="syntax"></a><span data-ttu-id="df8aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df8aa-105">Syntax</span></span>


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a><span data-ttu-id="df8aa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df8aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8aa-107">*курсорхидден*</span><span class="sxs-lookup"><span data-stu-id="df8aa-107">*CursorHidden*</span></span> 
</dt> <dd>

<span data-ttu-id="df8aa-108">Указатель на значение **m \_ бкурсорхидден**.</span><span class="sxs-lookup"><span data-stu-id="df8aa-108">Pointer to the value of **m\_bCursorHidden**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8aa-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df8aa-109">Return value</span></span>

<span data-ttu-id="df8aa-110">При вызове без параметра возвращает ОАТРУЕ, если курсор скрыт, или ОАФАЛСЕ, если курсор является видимым.</span><span class="sxs-lookup"><span data-stu-id="df8aa-110">When called without a parameter, returns OATRUE if the cursor is hidden, or OAFALSE if the cursor is visible.</span></span>

## <a name="remarks"></a><span data-ttu-id="df8aa-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df8aa-111">Remarks</span></span>

<span data-ttu-id="df8aa-112">Внутренние объекты должны вызывать эту функцию члена без параметра *курсорхидден* , чтобы избежать блокировки критической секции.</span><span class="sxs-lookup"><span data-stu-id="df8aa-112">Internal objects should call this member function without the *CursorHidden* parameter to avoid locking the critical section.</span></span> <span data-ttu-id="df8aa-113">Внешние объекты обращаются к этой функции-члену с помощью параметра *курсорхидден* с помощью метода [**Ивидеовиндов:: искурсорхидден**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .</span><span class="sxs-lookup"><span data-stu-id="df8aa-113">External objects access this member function with the *CursorHidden* parameter through the [**IVideoWindow::IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="df8aa-114">Требования</span><span class="sxs-lookup"><span data-stu-id="df8aa-114">Requirements</span></span>



| <span data-ttu-id="df8aa-115">Требование</span><span class="sxs-lookup"><span data-stu-id="df8aa-115">Requirement</span></span> | <span data-ttu-id="df8aa-116">Значение</span><span class="sxs-lookup"><span data-stu-id="df8aa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df8aa-117">Header</span><span class="sxs-lookup"><span data-stu-id="df8aa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="df8aa-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df8aa-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df8aa-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df8aa-119">Library</span></span><br/> | <dl> <span data-ttu-id="df8aa-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="df8aa-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8aa-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df8aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8aa-122">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="df8aa-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




