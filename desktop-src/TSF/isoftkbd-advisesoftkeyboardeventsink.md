---
title: Метод Исофткбд Адвисесофткэйбоардевентсинк (Софткбдк. h)
description: Метод Исофткбд Адвисесофткэйбоардевентсинк устанавливает приемник событий программируемой клавиатуры для управления уведомлениями Онкэйселектион от экранной клавиатуры.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Платформа служб текстового ввода метода Адвисесофткэйбоардевентсинк
- Платформа текстовых служб метода Адвисесофткэйбоардевентсинк, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Адвисесофткэйбоардевентсинк
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415924"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="a96b9-106">Метод Исофткбд:: Адвисесофткэйбоардевентсинк</span><span class="sxs-lookup"><span data-stu-id="a96b9-106">ISoftKbd::AdviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="a96b9-107">Метод **исофткбд:: адвисесофткэйбоардевентсинк** устанавливает приемник событий экранной клавиатуры для управления уведомлениями онкэйселектион от экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a96b9-107">The **ISoftKbd::AdviseSoftKeyboardEventSink** method installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="a96b9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a96b9-108">Syntax</span></span>


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a><span data-ttu-id="a96b9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a96b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a96b9-110">*двкэйбоардид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a96b9-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a96b9-111">Идентификатор программируемой клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a96b9-111">Identifier of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="a96b9-112">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a96b9-112">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a96b9-113">Идентификатор интерфейса для интерфейса приемника.</span><span class="sxs-lookup"><span data-stu-id="a96b9-113">Interface identifier for the sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="a96b9-114">*Punk* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a96b9-114">*punk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a96b9-115">Указатель на [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) для интерфейса приемника, заданного параметром *riid*.</span><span class="sxs-lookup"><span data-stu-id="a96b9-115">Pointer to [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) for the sink interface specified by *riid*.</span></span> <span data-ttu-id="a96b9-116">Этот параметр не может иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a96b9-116">This parameter cannot be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a96b9-117">*пдвкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a96b9-117">*pdwCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a96b9-118">Указатель на буфер, в котором этот метод получает программную клавиатуру "cookie", используемую для соединения с клиентом.</span><span class="sxs-lookup"><span data-stu-id="a96b9-118">Pointer to the buffer in which this method retrieves the soft keyboard "cookie" used for connection to the client.</span></span> <span data-ttu-id="a96b9-119">Файл cookie должен быть уникальным для каждого подключения.</span><span class="sxs-lookup"><span data-stu-id="a96b9-119">The cookie must be unique for each connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a96b9-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a96b9-120">Return value</span></span>

<span data-ttu-id="a96b9-121">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a96b9-121">This method can return one of these values.</span></span>



| <span data-ttu-id="a96b9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a96b9-122">Value</span></span>                                                                                        | <span data-ttu-id="a96b9-123">Описание</span><span class="sxs-lookup"><span data-stu-id="a96b9-123">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a96b9-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a96b9-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a96b9-125">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a96b9-125">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="a96b9-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a96b9-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a96b9-127">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="a96b9-127">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a96b9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a96b9-128">Requirements</span></span>



| <span data-ttu-id="a96b9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a96b9-129">Requirement</span></span> | <span data-ttu-id="a96b9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a96b9-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a96b9-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a96b9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a96b9-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a96b9-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a96b9-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a96b9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a96b9-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a96b9-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a96b9-135">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a96b9-135">Redistributable</span></span><br/>          | <span data-ttu-id="a96b9-136">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="a96b9-136">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a96b9-137">Header</span><span class="sxs-lookup"><span data-stu-id="a96b9-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a96b9-138"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="a96b9-138"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a96b9-139">IDL</span><span class="sxs-lookup"><span data-stu-id="a96b9-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a96b9-140"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a96b9-140"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a96b9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a96b9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a96b9-142"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a96b9-142"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a96b9-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a96b9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a96b9-144">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="a96b9-144">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="a96b9-145">**Исофткбд:: Унадвисесофткэйбоардевентсинк**</span><span class="sxs-lookup"><span data-stu-id="a96b9-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

