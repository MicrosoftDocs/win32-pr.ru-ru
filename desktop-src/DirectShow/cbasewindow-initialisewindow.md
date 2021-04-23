---
description: Метод Инитиалисевиндов инициализирует окно.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Iniметод Тиалисевиндов (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675469"
---
# <a name="cbasewindowinitialisewindow-method"></a><span data-ttu-id="28ac3-103">CBaseWindow.Iniметод Тиалисевиндов</span><span class="sxs-lookup"><span data-stu-id="28ac3-103">CBaseWindow.InitialiseWindow method</span></span>

<span data-ttu-id="28ac3-104">`InitialiseWindow`Метод инициализирует окно.</span><span class="sxs-lookup"><span data-stu-id="28ac3-104">The `InitialiseWindow` method initializes the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ac3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28ac3-105">Syntax</span></span>


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="28ac3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28ac3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ac3-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="28ac3-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="28ac3-108">Обработчик для окна.</span><span class="sxs-lookup"><span data-stu-id="28ac3-108">Handle to the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ac3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28ac3-109">Return value</span></span>

<span data-ttu-id="28ac3-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="28ac3-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="28ac3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28ac3-111">Remarks</span></span>

<span data-ttu-id="28ac3-112">По умолчанию этот метод получает маркер для контекста устройства (DC) окна и создает совместимый контроллер памяти.</span><span class="sxs-lookup"><span data-stu-id="28ac3-112">By default, this method retrieves a handle to the window's device context (DC) and creates a compatible memory DC.</span></span> <span data-ttu-id="28ac3-113">Однако если значение флага [**кбасевиндов:: m \_ Бдожетдк**](cbasewindow-m-bdogetdc.md) равно **false**, этот метод не извлекает контексты устройств.</span><span class="sxs-lookup"><span data-stu-id="28ac3-113">If the value of the [**CBaseWindow::m\_bDoGetDC**](cbasewindow-m-bdogetdc.md) flag is **FALSE**, however, this method does not retrieve the device contexts.</span></span> <span data-ttu-id="28ac3-114">КОНТРОЛЛЕР памяти может использоваться для выбора точечных рисунков, прежде чем блиттинг их в окно.</span><span class="sxs-lookup"><span data-stu-id="28ac3-114">The memory DC is useful for selecting bitmaps before blitting them to the window.</span></span>

<span data-ttu-id="28ac3-115">Метод [**кбасевиндов::D окреатевиндов**](cbasewindow-docreatewindow.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="28ac3-115">The [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ac3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="28ac3-116">Requirements</span></span>



| <span data-ttu-id="28ac3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="28ac3-117">Requirement</span></span> | <span data-ttu-id="28ac3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="28ac3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28ac3-119">Header</span><span class="sxs-lookup"><span data-stu-id="28ac3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="28ac3-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28ac3-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28ac3-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28ac3-121">Library</span></span><br/> | <dl> <span data-ttu-id="28ac3-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="28ac3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ac3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28ac3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ac3-124">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="28ac3-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




