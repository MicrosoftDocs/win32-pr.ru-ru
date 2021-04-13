---
title: Метод Исофткбд Селектсофткэйбоард (Софткбдк. h)
description: Метод Исофткбд Селектсофткэйбоард выбирает указанную мягкую клавиатуру.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Платформа служб текстового ввода метода Селектсофткэйбоард
- Платформа текстовых служб метода Селектсофткэйбоард, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Селектсофткэйбоард
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534901"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a><span data-ttu-id="bc36f-106">Метод Исофткбд:: Селектсофткэйбоард</span><span class="sxs-lookup"><span data-stu-id="bc36f-106">ISoftKbd::SelectSoftKeyboard method</span></span>

<span data-ttu-id="bc36f-107">Метод **исофткбд:: селектсофткэйбоард** выбирает указанную мягкую клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="bc36f-107">The **ISoftKbd::SelectSoftKeyboard** method selects the specified soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc36f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc36f-108">Syntax</span></span>


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a><span data-ttu-id="bc36f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc36f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc36f-110">*двкэйбоардид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc36f-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc36f-111">Идентификатор выбираемой загружаемой клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="bc36f-111">Identifier of the soft keyboard to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc36f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc36f-112">Return value</span></span>

<span data-ttu-id="bc36f-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="bc36f-113">This method can return one of these values.</span></span>



| <span data-ttu-id="bc36f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bc36f-114">Value</span></span>                                                                                        | <span data-ttu-id="bc36f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bc36f-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="bc36f-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bc36f-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bc36f-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="bc36f-117">The method was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="bc36f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bc36f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="bc36f-119">Недопустимый параметр *двкэйбоардид* .</span><span class="sxs-lookup"><span data-stu-id="bc36f-119">The *dwKeyboardId* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bc36f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="bc36f-120">Requirements</span></span>



| <span data-ttu-id="bc36f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="bc36f-121">Requirement</span></span> | <span data-ttu-id="bc36f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bc36f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc36f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc36f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc36f-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bc36f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bc36f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc36f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc36f-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bc36f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bc36f-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bc36f-127">Redistributable</span></span><br/>          | <span data-ttu-id="bc36f-128">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="bc36f-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="bc36f-129">Header</span><span class="sxs-lookup"><span data-stu-id="bc36f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc36f-130"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc36f-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="bc36f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="bc36f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc36f-132"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc36f-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="bc36f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bc36f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc36f-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc36f-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc36f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc36f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc36f-136">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="bc36f-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





