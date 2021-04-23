---
title: Метод Исофткбд Унадвисесофткэйбоардевентсинк (Софткбдк. h)
description: Метод Исофткбд Унадвисесофткэйбоардевентсинк удаляет многофункциональный приемник событий клавиатуры.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Платформа служб текстового ввода метода Унадвисесофткэйбоардевентсинк
- Платформа текстовых служб метода Унадвисесофткэйбоардевентсинк, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Унадвисесофткэйбоардевентсинк
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803239"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="1ea63-106">Метод Исофткбд:: Унадвисесофткэйбоардевентсинк</span><span class="sxs-lookup"><span data-stu-id="1ea63-106">ISoftKbd::UnadviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="1ea63-107">Метод **исофткбд:: унадвисесофткэйбоардевентсинк** удаляет приемник событий программируемой клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="1ea63-107">The **ISoftKbd::UnadviseSoftKeyboardEventSink** method removes a soft keyboard event sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea63-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ea63-108">Syntax</span></span>


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a><span data-ttu-id="1ea63-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ea63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ea63-110">*tid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ea63-110">*tid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea63-111">Идентификатор клиента, владеющего приемником событий программируемой клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="1ea63-111">Identifier of the client that owns the soft keyboard event sink.</span></span> <span data-ttu-id="1ea63-112">Это значение было передано при установке приемника событий с помощью [исофткбд:: адвисесофткэйбоардевентсинк](isoftkbd-advisesoftkeyboardeventsink.md).</span><span class="sxs-lookup"><span data-stu-id="1ea63-112">This value was passed when the event sink was installed using [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ea63-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ea63-113">Return value</span></span>

<span data-ttu-id="1ea63-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1ea63-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1ea63-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1ea63-115">Value</span></span>                                                                                                   | <span data-ttu-id="1ea63-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1ea63-116">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="1ea63-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea63-117"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="1ea63-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="1ea63-118">The method was successful.</span></span><br/>                         |
| <dl> <span data-ttu-id="1ea63-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea63-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="1ea63-120">Недопустимый параметр *tid* .</span><span class="sxs-lookup"><span data-stu-id="1ea63-120">The *tid* parameter is invalid.</span></span><br/>                    |
| <dl> <span data-ttu-id="1ea63-121"><dt>**подключение \_ к \_ соединению E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea63-121"><dt>**CONNECT\_E\_NOCONNECTION**</dt></span></span> </dl> | <span data-ttu-id="1ea63-122">Приемник уведомлений, идентифицируемый *tid* , не найден.</span><span class="sxs-lookup"><span data-stu-id="1ea63-122">The advise sink identified by *tid* was not found.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ea63-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1ea63-123">Requirements</span></span>



| <span data-ttu-id="1ea63-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1ea63-124">Requirement</span></span> | <span data-ttu-id="1ea63-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1ea63-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea63-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ea63-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ea63-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1ea63-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1ea63-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ea63-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ea63-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1ea63-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1ea63-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1ea63-130">Redistributable</span></span><br/>          | <span data-ttu-id="1ea63-131">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="1ea63-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="1ea63-132">Header</span><span class="sxs-lookup"><span data-stu-id="1ea63-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ea63-133"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ea63-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="1ea63-134">IDL</span><span class="sxs-lookup"><span data-stu-id="1ea63-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1ea63-135"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ea63-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="1ea63-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1ea63-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ea63-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ea63-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ea63-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ea63-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea63-139">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="1ea63-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="1ea63-140">Исофткбд:: Адвисесофткэйбоардевентсинк</span><span class="sxs-lookup"><span data-stu-id="1ea63-140">ISoftKbd::AdviseSoftKeyboardEventSink</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





