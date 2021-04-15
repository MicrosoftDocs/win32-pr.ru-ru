---
description: Обрабатывает состояние устройства и сообщения об ошибках во время передачи данных изображения и отображает сообщения для пользователя.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'Метод Ивиаапперрорхандлер:: Репортстатус (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701685"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a><span data-ttu-id="fc019-103">Метод Ивиаапперрорхандлер:: Репортстатус</span><span class="sxs-lookup"><span data-stu-id="fc019-103">IWiaAppErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="fc019-104">Обрабатывает состояние устройства и сообщения об ошибках во время передачи данных изображения и отображает сообщения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc019-104">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc019-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc019-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a><span data-ttu-id="fc019-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc019-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc019-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc019-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc019-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="fc019-108">Type: **LONG**</span></span>

<span data-ttu-id="fc019-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fc019-109">Not used.</span></span> <span data-ttu-id="fc019-110">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="fc019-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="fc019-111">*pWiaItem2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc019-111">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc019-112">Тип: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="fc019-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="fc019-113">Указатель на передаваемый элемент.</span><span class="sxs-lookup"><span data-stu-id="fc019-113">Pointer to the item being transferred.</span></span>

</dd> <dt>

<span data-ttu-id="fc019-114">_hrStatus \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="fc019-114">_hrStatus\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc019-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fc019-115">Type: **HRESULT**</span></span>

<span data-ttu-id="fc019-116">Код состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="fc019-116">Device status code.</span></span>

</dd> <dt>

<span data-ttu-id="fc019-117">*лперценткомплете* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc019-117">*lPercentComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc019-118">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="fc019-118">Type: **LONG**</span></span>

<span data-ttu-id="fc019-119">Процент завершения текущей операции.</span><span class="sxs-lookup"><span data-stu-id="fc019-119">Percentage completed of current operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc019-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc019-120">Return value</span></span>

<span data-ttu-id="fc019-121">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fc019-121">Type: **HRESULT**</span></span>

<span data-ttu-id="fc019-122">Возвращает *хрстатус* , если восстановление из ошибки невозможно.</span><span class="sxs-lookup"><span data-stu-id="fc019-122">Returns *hrStatus* if recovery from the error is not possible.</span></span> <span data-ttu-id="fc019-123">В противном случае возвращается одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fc019-123">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="fc019-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fc019-124">Return code</span></span>                                                                                              | <span data-ttu-id="fc019-125">Описание</span><span class="sxs-lookup"><span data-stu-id="fc019-125">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc019-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fc019-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="fc019-127">Если *хрстатус* является ошибкой, для исправления ошибки предпринимается соответствующее действие, а перемещение может быть продолжено.</span><span class="sxs-lookup"><span data-stu-id="fc019-127">If *hrStatus* is an error, the appropriate action was taken to correct the error, and the transfer can continue.</span></span> <span data-ttu-id="fc019-128">Если *хрстатус* является информационным, пользователь получил уведомление о немодальном диалоговом окне и отказался от отмены перемещения.</span><span class="sxs-lookup"><span data-stu-id="fc019-128">If *hrStatus* is informational, the user was informed with a modeless dialog box and chose not to cancel the transfer.</span></span><br/> |
| <dl> <span data-ttu-id="fc019-129"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="fc019-129"><dt>**S\_FALSE**</dt></span></span> </dl>                  | <span data-ttu-id="fc019-130">Пользователь отменил перемещение из немодального диалогового окна обработчика ошибок.</span><span class="sxs-lookup"><span data-stu-id="fc019-130">The user cancelled the transfer from the error handler modeless dialog box.</span></span> <span data-ttu-id="fc019-131">Это значение может возвращаться в любой момент, независимо от того, что *хрстатус* .</span><span class="sxs-lookup"><span data-stu-id="fc019-131">This value can be returned at any point no matter what *hrStatus* is.</span></span> <br/>                                                                                      |
| <dl> <span data-ttu-id="fc019-132"><dt>**\_состояние WIA \_ не \_ обработано**</dt></span><span class="sxs-lookup"><span data-stu-id="fc019-132"><dt>**WIA\_STATUS\_NOT\_HANDLED**</dt></span></span> </dl> | <span data-ttu-id="fc019-133">Никаких действий не выполнено; Это значит, что пользователю не было предоставлено диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fc019-133">No action was taken; that is, no dialog box was presented to the user.</span></span> <span data-ttu-id="fc019-134">Будет вызван следующий обработчик ошибок.</span><span class="sxs-lookup"><span data-stu-id="fc019-134">The next error handler will be invoked.</span></span> <span data-ttu-id="fc019-135">Порядок обработчиков ошибок: приложение, драйвер и система по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc019-135">The order of error handlers is: application, driver, and system default.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="fc019-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc019-136">Remarks</span></span>

<span data-ttu-id="fc019-137">Параметр *лперценткомплете* позволяет отображать ход выполнения в окне обработчика ошибок.</span><span class="sxs-lookup"><span data-stu-id="fc019-137">The *lPercentComplete* parameter enables an error handler window to show progress.</span></span> <span data-ttu-id="fc019-138">Например, драйвер может предоставить оценку того, сколько времени занимает "прогрев".</span><span class="sxs-lookup"><span data-stu-id="fc019-138">For example, a driver might provide an estimate of how long "warming up" takes.</span></span> <span data-ttu-id="fc019-139">Параметр *лперценткомплете* , передаваемый в **Ивиаапперрорхандлер:: репортстатус** , имеет то же значение, что и **лперценткомплете** , который драйвер задает в структуре [**виатрансферпарамс**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="fc019-139">The *lPercentComplete* parameter passed into **IWiaAppErrorHandler::ReportStatus** is the same value as the **lPercentComplete** that the driver sets into the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

<span data-ttu-id="fc019-140">Обработчик ошибок может использовать макросы Success и FAILed, чтобы выяснить, имеет ли *хрстатус* ошибку серьезности \_ или степень серьезности \_ .</span><span class="sxs-lookup"><span data-stu-id="fc019-140">An error handler can use the SUCCEEDED and FAILED macros to find out if *hrStatus* has SEVERITY\_ERROR or SEVERITY\_SUCCESS.</span></span>

<span data-ttu-id="fc019-141">Если *хрстатус* имеет серьезность \_ успеха, пользователю следует разрешить отменять перемещение.</span><span class="sxs-lookup"><span data-stu-id="fc019-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

<span data-ttu-id="fc019-142">Если *хрстатус* является ошибкой серьезности \_ , обработчик ошибок должен отобразить модальное диалоговое окно, принадлежащее родительскому окну приложения.</span><span class="sxs-lookup"><span data-stu-id="fc019-142">If *hrStatus* is SEVERITY\_ERROR, the error handler should display a modal dialog box owned by the application parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc019-143">Требования</span><span class="sxs-lookup"><span data-stu-id="fc019-143">Requirements</span></span>



| <span data-ttu-id="fc019-144">Требование</span><span class="sxs-lookup"><span data-stu-id="fc019-144">Requirement</span></span> | <span data-ttu-id="fc019-145">Значение</span><span class="sxs-lookup"><span data-stu-id="fc019-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc019-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc019-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fc019-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc019-147">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fc019-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc019-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fc019-149">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc019-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fc019-150">Header</span><span class="sxs-lookup"><span data-stu-id="fc019-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc019-151"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc019-151"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="fc019-152">IDL</span><span class="sxs-lookup"><span data-stu-id="fc019-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc019-153"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc019-153"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="fc019-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc019-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc019-155"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc019-155"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




