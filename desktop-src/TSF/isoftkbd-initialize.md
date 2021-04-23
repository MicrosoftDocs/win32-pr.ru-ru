---
title: Метод Initialize Исофткбд (Софткбдк. h)
description: Метод Initialize Исофткбд инициализирует все необходимые поля для мягкой клавиатуры и создает стандартные раскладки клавиатуры с мягкими клавиатурой.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Инициализация метода Text Services Framework
- Инициализация метода Text Services Framework, интерфейс Исофткбд
- Платформа текстовых служб с интерфейсом Исофткбд, метод Initialize
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801306"
---
# <a name="isoftkbdinitialize-method"></a><span data-ttu-id="abef9-106">Метод Исофткбд:: Initialize</span><span class="sxs-lookup"><span data-stu-id="abef9-106">ISoftKbd::Initialize method</span></span>

<span data-ttu-id="abef9-107">Метод **исофткбд:: Initialize** инициализирует все необходимые поля для мягкой клавиатуры и создает стандартные раскладки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="abef9-107">The **ISoftKbd::Initialize** method initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="abef9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abef9-108">Syntax</span></span>


```C++
HRESULT Initialize();
```



## <a name="parameters"></a><span data-ttu-id="abef9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="abef9-109">Parameters</span></span>

<span data-ttu-id="abef9-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="abef9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="abef9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abef9-111">Return value</span></span>

<span data-ttu-id="abef9-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="abef9-112">This method can return one of these values.</span></span>



| <span data-ttu-id="abef9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="abef9-113">Value</span></span>                                                                                | <span data-ttu-id="abef9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="abef9-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="abef9-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="abef9-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="abef9-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="abef9-116">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="abef9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="abef9-117">Requirements</span></span>



| <span data-ttu-id="abef9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="abef9-118">Requirement</span></span> | <span data-ttu-id="abef9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="abef9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abef9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abef9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="abef9-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="abef9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="abef9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abef9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="abef9-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="abef9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="abef9-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="abef9-124">Redistributable</span></span><br/>          | <span data-ttu-id="abef9-125">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="abef9-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="abef9-126">Header</span><span class="sxs-lookup"><span data-stu-id="abef9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="abef9-127"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="abef9-127"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="abef9-128">IDL</span><span class="sxs-lookup"><span data-stu-id="abef9-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abef9-129"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abef9-129"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="abef9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="abef9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abef9-131"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abef9-131"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abef9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abef9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abef9-133">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="abef9-133">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





