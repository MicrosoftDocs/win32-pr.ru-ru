---
title: Метод повторного подключения IMsRdpClient8
description: Повторно подключается к удаленному сеансу, используя новые значения ширины и высоты рабочего стола.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода повторного подключения
- Службы удаленных рабочих столов метода повторного подключения, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Reconnect
- Службы удаленных рабочих столов метода повторного подключения, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Reconnect
- Службы удаленных рабочих столов метода повторного подключения, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Reconnect
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535585"
---
# <a name="imsrdpclient8reconnect-method"></a><span data-ttu-id="a009f-110">Метод IMsRdpClient8:: Reconnect</span><span class="sxs-lookup"><span data-stu-id="a009f-110">IMsRdpClient8::Reconnect method</span></span>

<span data-ttu-id="a009f-111">Повторно подключается к удаленному сеансу, используя новые значения ширины и высоты рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="a009f-111">Reconnects to the remote session with the new desktop width and height.</span></span> <span data-ttu-id="a009f-112">Чтобы этот метод был выполнен, элемент управления уже должен быть подключен к удаленному сеансу.</span><span class="sxs-lookup"><span data-stu-id="a009f-112">The control must already be connected to a remote session for this method to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a009f-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a009f-113">Syntax</span></span>


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a009f-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="a009f-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a009f-115">*улвидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a009f-115">*ulWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a009f-116">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="a009f-116">Type: **ULONG**</span></span>

<span data-ttu-id="a009f-117">Новая ширина рабочего стола в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a009f-117">The new desktop width, in pixels.</span></span> <span data-ttu-id="a009f-118">См. свойство [**десктопвидс**](imstscax-desktopwidth.md) для ограничений по значению.</span><span class="sxs-lookup"><span data-stu-id="a009f-118">See the [**DesktopWidth**](imstscax-desktopwidth.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="a009f-119">*улхеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a009f-119">*ulHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a009f-120">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="a009f-120">Type: **ULONG**</span></span>

<span data-ttu-id="a009f-121">Новая высота рабочего стола (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="a009f-121">The new desktop height, in pixels.</span></span> <span data-ttu-id="a009f-122">См. свойство [**десктофеигхт**](imstscax-desktopheight.md) для ограничений по значению.</span><span class="sxs-lookup"><span data-stu-id="a009f-122">See the [**DesktopHeight**](imstscax-desktopheight.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="a009f-123">*преконнектстатус* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a009f-123">*pReconnectStatus* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a009f-124">Тип: \**[**контролреконнектстатус**](controlreconnectstatus.md) \** _</span><span class="sxs-lookup"><span data-stu-id="a009f-124">Type: \**[**ControlReconnectStatus**](controlreconnectstatus.md)\** _</span></span>

<span data-ttu-id="a009f-125">Указатель на переменную [_ *контролреконнектстатус* \*](controlreconnectstatus.md) , которая получает состояние операции повторного соединения.</span><span class="sxs-lookup"><span data-stu-id="a009f-125">A pointer to a [_ *ControlReconnectStatus*\*](controlreconnectstatus.md) variable that receives the status of the reconnect operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a009f-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a009f-126">Return value</span></span>

<span data-ttu-id="a009f-127">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a009f-127">Type: **HRESULT**</span></span>

<span data-ttu-id="a009f-128">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a009f-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a009f-129">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a009f-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a009f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="a009f-130">Requirements</span></span>



| <span data-ttu-id="a009f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="a009f-131">Requirement</span></span> | <span data-ttu-id="a009f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a009f-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a009f-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a009f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a009f-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a009f-134">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="a009f-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a009f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a009f-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a009f-136">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="a009f-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a009f-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a009f-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a009f-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a009f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a009f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a009f-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a009f-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a009f-141">IID</span><span class="sxs-lookup"><span data-stu-id="a009f-141">IID</span></span><br/>                      | <span data-ttu-id="a009f-142">IID \_ IMsRdpClient8 определен как 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="a009f-142">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a009f-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a009f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a009f-144">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a009f-144">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a009f-145">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a009f-145">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a009f-146">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a009f-146">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="a009f-147">**контролреконнектстатус**</span><span class="sxs-lookup"><span data-stu-id="a009f-147">**ControlReconnectStatus**</span></span>](controlreconnectstatus.md)
</dt> </dl>

 

 





