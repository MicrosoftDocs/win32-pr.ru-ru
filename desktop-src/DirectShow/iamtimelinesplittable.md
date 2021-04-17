---
description: Интерфейс Иамтимелинесплиттабле разделяет объект Timeline в службах редактирования DirectShow (DES). Этот интерфейс реализуется источниками, эффектами, переходами и дорожками.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Интерфейс Иамтимелинесплиттабле (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685084"
---
# <a name="iamtimelinesplittable-interface"></a><span data-ttu-id="dc54d-104">Интерфейс Иамтимелинесплиттабле</span><span class="sxs-lookup"><span data-stu-id="dc54d-104">IAMTimelineSplittable interface</span></span>

> [!Note]  
> <span data-ttu-id="dc54d-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="dc54d-105">\[Deprecated.</span></span> <span data-ttu-id="dc54d-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc54d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dc54d-107">`IAMTimelineSplittable`Интерфейс разделяет объект временной шкалы в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="dc54d-107">The `IAMTimelineSplittable` interface splits a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="dc54d-108">Этот интерфейс реализуется источниками, эффектами, переходами и дорожками.</span><span class="sxs-lookup"><span data-stu-id="dc54d-108">Sources, effects, transitions, and tracks implement this interface.</span></span>

## <a name="members"></a><span data-ttu-id="dc54d-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="dc54d-109">Members</span></span>

<span data-ttu-id="dc54d-110">Интерфейс **иамтимелинесплиттабле** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dc54d-110">The **IAMTimelineSplittable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc54d-111">**Иамтимелинесплиттабле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc54d-111">**IAMTimelineSplittable** also has these types of members:</span></span>

-   [<span data-ttu-id="dc54d-112">Методы</span><span class="sxs-lookup"><span data-stu-id="dc54d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc54d-113">Методы</span><span class="sxs-lookup"><span data-stu-id="dc54d-113">Methods</span></span>

<span data-ttu-id="dc54d-114">Интерфейс **иамтимелинесплиттабле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dc54d-114">The **IAMTimelineSplittable** interface has these methods.</span></span>



| <span data-ttu-id="dc54d-115">Метод</span><span class="sxs-lookup"><span data-stu-id="dc54d-115">Method</span></span>                                             | <span data-ttu-id="dc54d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dc54d-116">Description</span></span>                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc54d-117">**сплитат**</span><span class="sxs-lookup"><span data-stu-id="dc54d-117">**SplitAt**</span></span>](iamtimelinesplittable-splitat.md)   | <span data-ttu-id="dc54d-118">Разделяет объект в указанное время.</span><span class="sxs-lookup"><span data-stu-id="dc54d-118">Splits the object at the specified time.</span></span><br/>                                                  |
| [<span data-ttu-id="dc54d-119">**SplitAt2**</span><span class="sxs-lookup"><span data-stu-id="dc54d-119">**SplitAt2**</span></span>](iamtimelinesplittable-splitat2.md) | <span data-ttu-id="dc54d-120">Разделяет объект в указанное время, заданное как значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="dc54d-120">Splits the object at the specified time, specified as a [**REFTIME**](reftime.md) value.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc54d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc54d-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dc54d-122">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="dc54d-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dc54d-123">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc54d-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dc54d-124">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dc54d-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dc54d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dc54d-125">Requirements</span></span>



| <span data-ttu-id="dc54d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dc54d-126">Requirement</span></span> | <span data-ttu-id="dc54d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dc54d-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc54d-128">Header</span><span class="sxs-lookup"><span data-stu-id="dc54d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="dc54d-129"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc54d-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dc54d-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc54d-130">Library</span></span><br/> | <dl> <span data-ttu-id="dc54d-131"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc54d-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
