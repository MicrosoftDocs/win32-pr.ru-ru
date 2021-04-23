---
title: Метод Исофткбд Дестройсофткэйбоардвиндов (Софткбдк. h)
description: Метод Исофткбд Дестройсофткэйбоардвиндов уничтожает окно с экранной клавиатурой.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Платформа служб текстового ввода метода Дестройсофткэйбоардвиндов
- Платформа текстовых служб метода Дестройсофткэйбоардвиндов, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Дестройсофткэйбоардвиндов
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681897"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a><span data-ttu-id="29fc2-106">Исофткбд: метод:D Естройсофткэйбоардвиндов</span><span class="sxs-lookup"><span data-stu-id="29fc2-106">ISoftKbd::DestroySoftKeyboardWindow method</span></span>

<span data-ttu-id="29fc2-107">Метод **исофткбд::D естройсофткэйбоардвиндов** уничтожает окно с экранной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="29fc2-107">The **ISoftKbd::DestroySoftKeyboardWindow** method destroys a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="29fc2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29fc2-108">Syntax</span></span>


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a><span data-ttu-id="29fc2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="29fc2-109">Parameters</span></span>

<span data-ttu-id="29fc2-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="29fc2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29fc2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29fc2-111">Return value</span></span>

<span data-ttu-id="29fc2-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="29fc2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="29fc2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="29fc2-113">Value</span></span>                                                                                | <span data-ttu-id="29fc2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="29fc2-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="29fc2-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="29fc2-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="29fc2-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="29fc2-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29fc2-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29fc2-117">Remarks</span></span>

<span data-ttu-id="29fc2-118">Этот метод удаляет окно с экранной клавиатурой, созданное ранее с помощью вызова [**исофткбд:: креатесофткэйбоардвиндов**](isoftkbd-createsoftkeyboardwindow.md).</span><span class="sxs-lookup"><span data-stu-id="29fc2-118">This method removes a soft keyboard window previously created with a call to [**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29fc2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="29fc2-119">Requirements</span></span>



| <span data-ttu-id="29fc2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="29fc2-120">Requirement</span></span> | <span data-ttu-id="29fc2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="29fc2-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29fc2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29fc2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="29fc2-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29fc2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="29fc2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29fc2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="29fc2-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29fc2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="29fc2-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="29fc2-126">Redistributable</span></span><br/>          | <span data-ttu-id="29fc2-127">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="29fc2-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="29fc2-128">Header</span><span class="sxs-lookup"><span data-stu-id="29fc2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="29fc2-129"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="29fc2-129"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="29fc2-130">IDL</span><span class="sxs-lookup"><span data-stu-id="29fc2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="29fc2-131"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="29fc2-131"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="29fc2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="29fc2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29fc2-133"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29fc2-133"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29fc2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29fc2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29fc2-135">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="29fc2-135">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="29fc2-136">**Исофткбд:: Креатесофткэйбоардвиндов**</span><span class="sxs-lookup"><span data-stu-id="29fc2-136">**ISoftKbd::CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





