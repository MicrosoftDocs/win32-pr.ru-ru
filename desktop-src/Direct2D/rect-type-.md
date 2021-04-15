---
title: Функция типа Rect (D2d1helper. h)
description: Создает прямоугольную структуру, в которой хранятся координаты, используя указанный тип данных.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Тип Rect, функция Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654557"
---
# <a name="recttype-function"></a><span data-ttu-id="2a0c1-104">Rect, <Type> функция</span><span class="sxs-lookup"><span data-stu-id="2a0c1-104">Rect<Type> Function</span></span>

<span data-ttu-id="2a0c1-105">Создает прямоугольную структуру, в которой хранятся координаты, используя указанный тип данных.</span><span class="sxs-lookup"><span data-stu-id="2a0c1-105">Creates a rectangle structure that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a><span data-ttu-id="2a0c1-106">Параметры шаблона</span><span class="sxs-lookup"><span data-stu-id="2a0c1-106">Template Parameters</span></span>



| <span data-ttu-id="2a0c1-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="2a0c1-107">Parameter</span></span> | <span data-ttu-id="2a0c1-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2a0c1-108">Description</span></span>                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0c1-109">Тип</span><span class="sxs-lookup"><span data-stu-id="2a0c1-109">Type</span></span>      | <span data-ttu-id="2a0c1-110">Тип данных, используемый для хранения размеров прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2a0c1-110">The data type used to store the dimensions of the rectangle.</span></span> <span data-ttu-id="2a0c1-111">Возможными значениями являются **float** и **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="2a0c1-111">Possible values are **FLOAT** and **UINT32**.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="2a0c1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a0c1-112">Parameters</span></span>



| <span data-ttu-id="2a0c1-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="2a0c1-113">Parameter</span></span> | <span data-ttu-id="2a0c1-114">Описание:</span><span class="sxs-lookup"><span data-stu-id="2a0c1-114">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="2a0c1-115">Левое</span><span class="sxs-lookup"><span data-stu-id="2a0c1-115">left</span></span>      | <span data-ttu-id="2a0c1-116">Координата по оси x верхнего левого угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2a0c1-116">The x-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="2a0c1-117">top</span><span class="sxs-lookup"><span data-stu-id="2a0c1-117">top</span></span>       | <span data-ttu-id="2a0c1-118">Координата по оси y верхнего левого угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2a0c1-118">The y-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="2a0c1-119">right</span><span class="sxs-lookup"><span data-stu-id="2a0c1-119">right</span></span>     | <span data-ttu-id="2a0c1-120">Координата по оси x правого нижнего угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2a0c1-120">The x-coordinate of the rectangle's lower-right corner.</span></span> |
| <span data-ttu-id="2a0c1-121">снизу</span><span class="sxs-lookup"><span data-stu-id="2a0c1-121">bottom</span></span>    | <span data-ttu-id="2a0c1-122">Координата по оси y правого нижнего угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2a0c1-122">The y-coordinate of the rectangle's lower-right corner.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="2a0c1-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a0c1-123">Return Value</span></span>

<span data-ttu-id="2a0c1-124">Структура прямоугольника, которая содержит указанные координаты.</span><span class="sxs-lookup"><span data-stu-id="2a0c1-124">A rectangle structure that contains the specified coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a0c1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2a0c1-125">Requirements</span></span>



| <span data-ttu-id="2a0c1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2a0c1-126">Requirement</span></span> | <span data-ttu-id="2a0c1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0c1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0c1-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a0c1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2a0c1-129">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a0c1-129">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2a0c1-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a0c1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2a0c1-131">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a0c1-131">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2a0c1-132">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="2a0c1-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2a0c1-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="2a0c1-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="2a0c1-134">Header</span><span class="sxs-lookup"><span data-stu-id="2a0c1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a0c1-135"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a0c1-135"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="2a0c1-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a0c1-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a0c1-137"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a0c1-137"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="2a0c1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2a0c1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a0c1-139"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a0c1-139"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





