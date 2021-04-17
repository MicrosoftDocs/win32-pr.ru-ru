---
description: Интерфейс Иамтимелиневиртуалтракк предоставляет методы для работы с виртуальными дорожками в службах редактирования DirectShow (DES). Этот интерфейс поддерживается композициями и дорожками.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Интерфейс Иамтимелиневиртуалтракк (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685437"
---
# <a name="iamtimelinevirtualtrack-interface"></a><span data-ttu-id="467bc-104">Интерфейс Иамтимелиневиртуалтракк</span><span class="sxs-lookup"><span data-stu-id="467bc-104">IAMTimelineVirtualTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="467bc-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="467bc-105">\[Deprecated.</span></span> <span data-ttu-id="467bc-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="467bc-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="467bc-107">`IAMTimelineVirtualTrack`Интерфейс предоставляет методы для работы с виртуальными дорожками в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="467bc-107">The `IAMTimelineVirtualTrack` interface provides methods for working with virtual tracks in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="467bc-108">Этот интерфейс поддерживается композициями и дорожками.</span><span class="sxs-lookup"><span data-stu-id="467bc-108">Compositions and tracks support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="467bc-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="467bc-109">Members</span></span>

<span data-ttu-id="467bc-110">Интерфейс **иамтимелиневиртуалтракк** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="467bc-110">The **IAMTimelineVirtualTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="467bc-111">**Иамтимелиневиртуалтракк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="467bc-111">**IAMTimelineVirtualTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="467bc-112">Методы</span><span class="sxs-lookup"><span data-stu-id="467bc-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="467bc-113">Методы</span><span class="sxs-lookup"><span data-stu-id="467bc-113">Methods</span></span>

<span data-ttu-id="467bc-114">Интерфейс **иамтимелиневиртуалтракк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="467bc-114">The **IAMTimelineVirtualTrack** interface has these methods.</span></span>



| <span data-ttu-id="467bc-115">Метод</span><span class="sxs-lookup"><span data-stu-id="467bc-115">Method</span></span>                                                               | <span data-ttu-id="467bc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="467bc-116">Description</span></span>                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="467bc-117">**сеттраккдирти**</span><span class="sxs-lookup"><span data-stu-id="467bc-117">**SetTrackDirty**</span></span>](iamtimelinevirtualtrack-settrackdirty.md)       | <span data-ttu-id="467bc-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="467bc-118">Not supported.</span></span><br/>                         |
| [<span data-ttu-id="467bc-119">**траккжетприорити**</span><span class="sxs-lookup"><span data-stu-id="467bc-119">**TrackGetPriority**</span></span>](iamtimelinevirtualtrack-trackgetpriority.md) | <span data-ttu-id="467bc-120">Возвращает уровень приоритета объекта.</span><span class="sxs-lookup"><span data-stu-id="467bc-120">Retrieves the object's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="467bc-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="467bc-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="467bc-122">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="467bc-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="467bc-123">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="467bc-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="467bc-124">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="467bc-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="467bc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="467bc-125">Requirements</span></span>



| <span data-ttu-id="467bc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="467bc-126">Requirement</span></span> | <span data-ttu-id="467bc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="467bc-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="467bc-128">Header</span><span class="sxs-lookup"><span data-stu-id="467bc-128">Header</span></span><br/>  | <dl> <span data-ttu-id="467bc-129"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="467bc-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="467bc-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="467bc-130">Library</span></span><br/> | <dl> <span data-ttu-id="467bc-131"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="467bc-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
