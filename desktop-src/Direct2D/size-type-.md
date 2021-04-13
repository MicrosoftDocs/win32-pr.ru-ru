---
title: Функция типа size (D2d1helper. h)
description: Создает структуру размера, в которой хранятся значения ширины и высоты, используя указанный тип данных.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Тип размера функция Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490149"
---
# <a name="sizetype-function"></a><span data-ttu-id="0afca-104">Size, <Type> функция</span><span class="sxs-lookup"><span data-stu-id="0afca-104">Size<Type> Function</span></span>

<span data-ttu-id="0afca-105">Создает структуру размера, в которой хранятся значения ширины и высоты, используя указанный тип данных.</span><span class="sxs-lookup"><span data-stu-id="0afca-105">Creates a size structure that stores its width and height using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a><span data-ttu-id="0afca-106">Параметры шаблона</span><span class="sxs-lookup"><span data-stu-id="0afca-106">Template Parameters</span></span>



| <span data-ttu-id="0afca-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="0afca-107">Parameter</span></span> | <span data-ttu-id="0afca-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0afca-108">Description</span></span>                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0afca-109">Тип</span><span class="sxs-lookup"><span data-stu-id="0afca-109">Type</span></span>      | <span data-ttu-id="0afca-110">Тип данных, используемый для хранения ширины и высоты размера.</span><span class="sxs-lookup"><span data-stu-id="0afca-110">The data type used to store the width and height of the size.</span></span> <span data-ttu-id="0afca-111">Возможными значениями являются FLOAT и UINT32.</span><span class="sxs-lookup"><span data-stu-id="0afca-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="0afca-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0afca-112">Parameters</span></span>



| <span data-ttu-id="0afca-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="0afca-113">Parameter</span></span> | <span data-ttu-id="0afca-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0afca-114">Description</span></span>        |
|-----------|--------------------|
| <span data-ttu-id="0afca-115">width</span><span class="sxs-lookup"><span data-stu-id="0afca-115">width</span></span>     | <span data-ttu-id="0afca-116">Ширина размера.</span><span class="sxs-lookup"><span data-stu-id="0afca-116">The size's width.</span></span>  |
| <span data-ttu-id="0afca-117">рост</span><span class="sxs-lookup"><span data-stu-id="0afca-117">height</span></span>    | <span data-ttu-id="0afca-118">Высота размера.</span><span class="sxs-lookup"><span data-stu-id="0afca-118">The size's height.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="0afca-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0afca-119">Return Value</span></span>

<span data-ttu-id="0afca-120">Размер, который содержит указанные ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="0afca-120">A size that contains the specified width and height.</span></span>

## <a name="requirements"></a><span data-ttu-id="0afca-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0afca-121">Requirements</span></span>



| <span data-ttu-id="0afca-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0afca-122">Requirement</span></span> | <span data-ttu-id="0afca-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0afca-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0afca-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0afca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0afca-125">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="0afca-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="0afca-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0afca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0afca-127">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0afca-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="0afca-128">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="0afca-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="0afca-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="0afca-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="0afca-130">Header</span><span class="sxs-lookup"><span data-stu-id="0afca-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0afca-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="0afca-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="0afca-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0afca-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0afca-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0afca-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="0afca-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0afca-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0afca-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0afca-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





