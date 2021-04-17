---
description: Обрабатывает сообщения о состоянии и ошибках во время передачи данных изображения и отображает их пользователю.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'Метод Ивиаеррорхандлер:: Репортстатус (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663393"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a><span data-ttu-id="ec500-103">Метод Ивиаеррорхандлер:: Репортстатус</span><span class="sxs-lookup"><span data-stu-id="ec500-103">IWiaErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="ec500-104">Обрабатывает сообщения о состоянии и ошибках во время передачи данных изображения и отображает их пользователю.</span><span class="sxs-lookup"><span data-stu-id="ec500-104">Handles status and error messages during image data transfers and displays them to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec500-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec500-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a><span data-ttu-id="ec500-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec500-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec500-107">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec500-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec500-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="ec500-108">Type: **HWND**</span></span>

<span data-ttu-id="ec500-109">**HWND** , который является родительским окном для окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="ec500-109">**HWND** that is the parent window for the message window.</span></span>

</dd> <dt>

<span data-ttu-id="ec500-110">*пункитем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec500-110">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec500-111">Тип: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="ec500-111">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="ec500-112">Указатель на интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) переносимого элемента.</span><span class="sxs-lookup"><span data-stu-id="ec500-112">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the item being transferred.</span></span> <span data-ttu-id="ec500-113">Этот объект минимальное реализует [_ *IWiaItem2* \*](-wia-iwiaitem2.md) и [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="ec500-113">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="ec500-114">*хрстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec500-114">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec500-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ec500-115">Type: **HRESULT**</span></span>

<span data-ttu-id="ec500-116">**Значение HRESULT** , которое является кодом состояния, полученным [**бандеддатакаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="ec500-116">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="ec500-117">*кбресленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec500-117">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec500-118">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="ec500-118">Type: **LONG**</span></span>

<span data-ttu-id="ec500-119">Значение **типа Long** , равное размеру данных, на которые ссылается *pbData*.</span><span class="sxs-lookup"><span data-stu-id="ec500-119">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="ec500-120">*pbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec500-120">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec500-121">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="ec500-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="ec500-122">Указатель на буфер данных, полученный с помощью [_ *бандеддатакаллбакк* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="ec500-122">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec500-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec500-123">Return value</span></span>

<span data-ttu-id="ec500-124">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ec500-124">Type: **HRESULT**</span></span>

<span data-ttu-id="ec500-125">Возвращает *хрстатус* , если ошибка не может быть восстановлена из.</span><span class="sxs-lookup"><span data-stu-id="ec500-125">Returns *hrStatus* if the error cannot be recovered from.</span></span> <span data-ttu-id="ec500-126">В противном случае возвращается одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ec500-126">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="ec500-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ec500-127">Return code</span></span>                                                                             | <span data-ttu-id="ec500-128">Описание</span><span class="sxs-lookup"><span data-stu-id="ec500-128">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec500-129"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ec500-129"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ec500-130">Было предпринято действие по исправлению ошибки, и перемещение может быть продолжено.</span><span class="sxs-lookup"><span data-stu-id="ec500-130">The appropriate action was taken to correct the error and the transfer can continue.</span></span> <br/> |
| <dl> <span data-ttu-id="ec500-131"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ec500-131"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ec500-132">Не было предпринято никаких действий по обработке ошибки или состояния отчета для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ec500-132">No action was taken to handle the error or report status to the user.</span></span> <br/>                |
| <dl> <span data-ttu-id="ec500-133"><dt>**\_прервать**</dt></span><span class="sxs-lookup"><span data-stu-id="ec500-133"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="ec500-134">Пользователь решил отменить перемещение в ответ на отображаемое диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ec500-134">The user chose to abort the transfer in response to the displayed dialog box.</span></span> <br/>        |



 

## <a name="remarks"></a><span data-ttu-id="ec500-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec500-135">Remarks</span></span>

<span data-ttu-id="ec500-136">Получение образа Windows (WIA) 2,0 вызывает **ивиаеррорхандлер:: репортстатус** , когда драйвер отправляет сообщение **\_ \_ \_ о состоянии устройства MSG** в [**бандеддатакаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="ec500-136">Windows Image Acquisition (WIA) 2.0 calls **IWiaErrorHandler::ReportStatus** when the driver sends an **IT\_MSG\_DEVICE\_STATUS** message to [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span> <span data-ttu-id="ec500-137">Этот метод обрабатывает сообщение и отображает сведения о состоянии или ошибке для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ec500-137">This method handles the message and displays information to the user about the status or error.</span></span> <span data-ttu-id="ec500-138">Если сообщение относится к ошибке, метод позволяет пользователю выбрать, если возможно, попытаться выполнить восстановление после ошибки и продолжить перемещение или прервать его.</span><span class="sxs-lookup"><span data-stu-id="ec500-138">If the message is about an error, the method lets the user choose, if possible, whether to try to recover from the error and continue the transfer or to abort.</span></span>

<span data-ttu-id="ec500-139">для *хрстатус* задано значение " \_ Перенос состояния WIA \_ \_ " начинается с уведомления обработчика о начале передачи.</span><span class="sxs-lookup"><span data-stu-id="ec500-139">*hrStatus* is set to WIA\_STATUS\_TRANSFER\_BEGIN to inform the handler a transfer has started.</span></span> <span data-ttu-id="ec500-140">\_ \_ После завершения перемещения для него задается состояние WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="ec500-140">It is set to WIA\_STATUS\_TRANSFER\_END when the transfer is complete.</span></span>

<span data-ttu-id="ec500-141">Если *хрстатус* имеет серьезность \_ успеха, пользователю следует разрешить отменять перемещение.</span><span class="sxs-lookup"><span data-stu-id="ec500-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec500-142">Требования</span><span class="sxs-lookup"><span data-stu-id="ec500-142">Requirements</span></span>



| <span data-ttu-id="ec500-143">Требование</span><span class="sxs-lookup"><span data-stu-id="ec500-143">Requirement</span></span> | <span data-ttu-id="ec500-144">Значение</span><span class="sxs-lookup"><span data-stu-id="ec500-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec500-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec500-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ec500-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec500-146">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ec500-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec500-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ec500-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ec500-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ec500-149">Header</span><span class="sxs-lookup"><span data-stu-id="ec500-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec500-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec500-150"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="ec500-151">IDL</span><span class="sxs-lookup"><span data-stu-id="ec500-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ec500-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ec500-152"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="ec500-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ec500-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="ec500-154"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec500-154"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
