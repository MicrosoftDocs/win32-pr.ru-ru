---
title: Функция типа Point2 (D2d1helper. h)
description: Создает точку, в которой хранятся координаты, используя указанный тип данных.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Функция типа Point2 Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654558"
---
# <a name="point2type-function"></a><span data-ttu-id="2ae2f-104"><Type>Функция Point2</span><span class="sxs-lookup"><span data-stu-id="2ae2f-104">Point2<Type> Function</span></span>

<span data-ttu-id="2ae2f-105">Создает точку, в которой хранятся координаты, используя указанный тип данных.</span><span class="sxs-lookup"><span data-stu-id="2ae2f-105">Creates a point that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a><span data-ttu-id="2ae2f-106">Параметры шаблона</span><span class="sxs-lookup"><span data-stu-id="2ae2f-106">Template Parameters</span></span>



| <span data-ttu-id="2ae2f-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="2ae2f-107">Parameter</span></span> | <span data-ttu-id="2ae2f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2ae2f-108">Description</span></span>                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae2f-109">Тип</span><span class="sxs-lookup"><span data-stu-id="2ae2f-109">Type</span></span>      | <span data-ttu-id="2ae2f-110">Тип данных, используемый для хранения координаты x и координаты y точки.</span><span class="sxs-lookup"><span data-stu-id="2ae2f-110">The data type used to store the x-coordinate and y-coordinate of the point.</span></span> <span data-ttu-id="2ae2f-111">Возможными значениями являются FLOAT и UINT32.</span><span class="sxs-lookup"><span data-stu-id="2ae2f-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="2ae2f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ae2f-112">Parameters</span></span>



| <span data-ttu-id="2ae2f-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="2ae2f-113">Parameter</span></span> | <span data-ttu-id="2ae2f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2ae2f-114">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="2ae2f-115">x</span><span class="sxs-lookup"><span data-stu-id="2ae2f-115">x</span></span>         | <span data-ttu-id="2ae2f-116">Координата X точки.</span><span class="sxs-lookup"><span data-stu-id="2ae2f-116">The x-coordinate of the point.</span></span> |
| <span data-ttu-id="2ae2f-117">да</span><span class="sxs-lookup"><span data-stu-id="2ae2f-117">y</span></span>         | <span data-ttu-id="2ae2f-118">Координата Y точки.</span><span class="sxs-lookup"><span data-stu-id="2ae2f-118">The y-coordinate of the point.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="2ae2f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ae2f-119">Return Value</span></span>

<span data-ttu-id="2ae2f-120">Точка, которая содержит заданную координату x и y.</span><span class="sxs-lookup"><span data-stu-id="2ae2f-120">A point that contains the specified x-coordinate and y-coordinate.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae2f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2ae2f-121">Requirements</span></span>



| <span data-ttu-id="2ae2f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2ae2f-122">Requirement</span></span> | <span data-ttu-id="2ae2f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae2f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae2f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ae2f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae2f-125">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="2ae2f-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2ae2f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ae2f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae2f-127">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2ae2f-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2ae2f-128">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="2ae2f-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2ae2f-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="2ae2f-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="2ae2f-130">Header</span><span class="sxs-lookup"><span data-stu-id="2ae2f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ae2f-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae2f-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="2ae2f-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ae2f-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ae2f-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ae2f-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="2ae2f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2ae2f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ae2f-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ae2f-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





