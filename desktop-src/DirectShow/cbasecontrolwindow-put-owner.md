---
description: Метод постановки \_ владельца задает родительское окно видео, а родительское окно пересылает определенные сообщения в окно видео.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Метод CBaseControlWindow.put_Owner (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657866"
---
# <a name="cbasecontrolwindowput_owner-method"></a><span data-ttu-id="358ae-103">Кбасеконтролвиндов. размещение, \_ метод Owner</span><span class="sxs-lookup"><span data-stu-id="358ae-103">CBaseControlWindow.put\_Owner method</span></span>

<span data-ttu-id="358ae-104">`put_Owner`Метод задает родительское окно видео, а затем родительское окно перенаправляет определенные сообщения в окно видео.</span><span class="sxs-lookup"><span data-stu-id="358ae-104">The `put_Owner` method sets the video window's parent window; the parent window then forwards certain messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="358ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="358ae-105">Syntax</span></span>


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a><span data-ttu-id="358ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="358ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="358ae-107">*Владелец*</span><span class="sxs-lookup"><span data-stu-id="358ae-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="358ae-108">Дескриптор родительского окна.</span><span class="sxs-lookup"><span data-stu-id="358ae-108">Handle to the parent window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="358ae-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="358ae-109">Return value</span></span>

<span data-ttu-id="358ae-110">Возвращает значение "ошибка".</span><span class="sxs-lookup"><span data-stu-id="358ae-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="358ae-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="358ae-111">Remarks</span></span>

<span data-ttu-id="358ae-112">На внутреннем уровне этот метод вызывает функцию Microsoft Win32 **сетпарент** для установки нового владельца и задает для родительского окна стиль \_ дочерний элемент WS.</span><span class="sxs-lookup"><span data-stu-id="358ae-112">Internally, this method calls the Microsoft Win32 **SetParent** function to set the new owner and sets the parent window's style to WS\_CHILD.</span></span> <span data-ttu-id="358ae-113">Затем родительское окно будет пересылать определенные наборы сообщений (в частности, мыши и клавиатуры) в окно видео.</span><span class="sxs-lookup"><span data-stu-id="358ae-113">The parent window will then forward certain sets of messages (in particular, mouse and keyboard messages) to the video window.</span></span>

<span data-ttu-id="358ae-114">После задания владельца видеоокна необходимо присвоить владельцу **значение NULL** , а в стиле окна владельца — WS \_ OVERLAPPED and WS \_ клипчилдрен, прежде чем выпустить граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="358ae-114">After you set the video window's owner, you must set the owner to **NULL** and the owner's window style to WS\_OVERLAPPED and WS\_CLIPCHILDREN before releasing the filter graph.</span></span> <span data-ttu-id="358ae-115">Если для владельца задано **значение NULL**, этот метод отключает \_ дочерний бит WS родительского окна.</span><span class="sxs-lookup"><span data-stu-id="358ae-115">When you set the owner to **NULL**, this method turns off the parent window's WS\_CHILD bit.</span></span> <span data-ttu-id="358ae-116">Если не задать для владельца **значение NULL**, то родительское окно продолжит передавать сообщения в окно видео, и ошибки, скорее всего, будут возникать при закрытии приложения.</span><span class="sxs-lookup"><span data-stu-id="358ae-116">If you don't set the owner to **NULL**, the parent window will continue to pass messages to the video window and errors will likely occur when the application closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="358ae-117">Требования</span><span class="sxs-lookup"><span data-stu-id="358ae-117">Requirements</span></span>



| <span data-ttu-id="358ae-118">Требование</span><span class="sxs-lookup"><span data-stu-id="358ae-118">Requirement</span></span> | <span data-ttu-id="358ae-119">Значение</span><span class="sxs-lookup"><span data-stu-id="358ae-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="358ae-120">Header</span><span class="sxs-lookup"><span data-stu-id="358ae-120">Header</span></span><br/>  | <dl> <span data-ttu-id="358ae-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="358ae-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="358ae-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="358ae-122">Library</span></span><br/> | <dl> <span data-ttu-id="358ae-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="358ae-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="358ae-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="358ae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="358ae-125">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="358ae-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




