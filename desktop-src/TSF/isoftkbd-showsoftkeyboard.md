---
title: Метод Исофткбд Шовсофткэйбоард (Софткбдк. h)
description: Метод Исофткбд Шовсофткэйбоард отображает экранную клавиатуру.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- Платформа служб текстового ввода метода Шовсофткэйбоард
- Платформа текстовых служб метода Шовсофткэйбоард, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Шовсофткэйбоард
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071078"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a><span data-ttu-id="f9f94-106">Метод Исофткбд:: Шовсофткэйбоард</span><span class="sxs-lookup"><span data-stu-id="f9f94-106">ISoftKbd::ShowSoftKeyboard method</span></span>

<span data-ttu-id="f9f94-107">Метод **исофткбд:: шовсофткэйбоард** отображает экранную клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="f9f94-107">The **ISoftKbd::ShowSoftKeyboard** method displays a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f94-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9f94-108">Syntax</span></span>


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a><span data-ttu-id="f9f94-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9f94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9f94-110">*ишов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9f94-110">*iShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9f94-111">Целое число, указывающее тип отображаемой экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="f9f94-111">Integer indicating the type of soft keyboard to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9f94-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9f94-112">Return value</span></span>

<span data-ttu-id="f9f94-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f9f94-113">This method can return one of these values.</span></span>



| <span data-ttu-id="f9f94-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f9f94-114">Value</span></span>                                                                                | <span data-ttu-id="f9f94-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f9f94-115">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f9f94-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f94-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f9f94-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f9f94-117">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f9f94-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f9f94-118">Requirements</span></span>



| <span data-ttu-id="f9f94-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f9f94-119">Requirement</span></span> | <span data-ttu-id="f9f94-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f9f94-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f94-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9f94-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f94-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9f94-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f9f94-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9f94-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f94-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9f94-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f9f94-125">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f9f94-125">Redistributable</span></span><br/>          | <span data-ttu-id="f9f94-126">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="f9f94-126">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f9f94-127">Header</span><span class="sxs-lookup"><span data-stu-id="f9f94-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9f94-128"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9f94-128"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f9f94-129">IDL</span><span class="sxs-lookup"><span data-stu-id="f9f94-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9f94-130"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9f94-130"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f9f94-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f9f94-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9f94-132"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9f94-132"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9f94-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9f94-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f94-134">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="f9f94-134">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





