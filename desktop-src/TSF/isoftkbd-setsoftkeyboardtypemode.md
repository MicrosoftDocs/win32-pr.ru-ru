---
title: Метод Исофткбд Сетсофткэйбоардтипемоде (Софткбдк. h)
description: Метод Исофткбд Сетсофткэйбоардтипемоде задает режим типа для экранной клавиатуры.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Платформа служб текстового ввода метода Сетсофткэйбоардтипемоде
- Платформа текстовых служб метода Сетсофткэйбоардтипемоде, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Сетсофткэйбоардтипемоде
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492102"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a><span data-ttu-id="afdcc-106">Метод Исофткбд:: Сетсофткэйбоардтипемоде</span><span class="sxs-lookup"><span data-stu-id="afdcc-106">ISoftKbd::SetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="afdcc-107">Метод **исофткбд:: сетсофткэйбоардтипемоде** задает режим типа для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="afdcc-107">The **ISoftKbd::SetSoftKeyboardTypeMode** method sets the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="afdcc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afdcc-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="afdcc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="afdcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afdcc-110">*Типемоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afdcc-110">*TypeMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afdcc-111">Режим типа.</span><span class="sxs-lookup"><span data-stu-id="afdcc-111">The type mode.</span></span> <span data-ttu-id="afdcc-112">Для перечисления [**типемоде**](typemode.md) определены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="afdcc-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afdcc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afdcc-113">Return value</span></span>

<span data-ttu-id="afdcc-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="afdcc-114">This method can return one of these values.</span></span>



| <span data-ttu-id="afdcc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="afdcc-115">Value</span></span>                                                                                        | <span data-ttu-id="afdcc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="afdcc-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="afdcc-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="afdcc-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="afdcc-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="afdcc-118">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="afdcc-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="afdcc-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="afdcc-120">Недопустимый параметр *типемоде* .</span><span class="sxs-lookup"><span data-stu-id="afdcc-120">The *TypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="afdcc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="afdcc-121">Requirements</span></span>



| <span data-ttu-id="afdcc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="afdcc-122">Requirement</span></span> | <span data-ttu-id="afdcc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="afdcc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afdcc-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afdcc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="afdcc-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="afdcc-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="afdcc-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afdcc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="afdcc-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="afdcc-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="afdcc-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="afdcc-128">Redistributable</span></span><br/>          | <span data-ttu-id="afdcc-129">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="afdcc-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="afdcc-130">Header</span><span class="sxs-lookup"><span data-stu-id="afdcc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="afdcc-131"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="afdcc-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="afdcc-132">IDL</span><span class="sxs-lookup"><span data-stu-id="afdcc-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afdcc-133"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afdcc-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="afdcc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="afdcc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afdcc-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afdcc-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afdcc-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afdcc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afdcc-137">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="afdcc-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="afdcc-138">**Исофткбд:: Жетсофткэйбоардтипемоде**</span><span class="sxs-lookup"><span data-stu-id="afdcc-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="afdcc-139">**типемоде**</span><span class="sxs-lookup"><span data-stu-id="afdcc-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





