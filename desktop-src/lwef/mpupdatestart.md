---
title: Функция Мпупдатестарт (Мпклиент. h)
description: Запускает операцию обновления сигнатур.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Функции Мпупдатестарт устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492627"
---
# <a name="mpupdatestart-function"></a><span data-ttu-id="e254f-104">Функция Мпупдатестарт</span><span class="sxs-lookup"><span data-stu-id="e254f-104">MpUpdateStart function</span></span>

<span data-ttu-id="e254f-105">Запускает операцию обновления сигнатур.</span><span class="sxs-lookup"><span data-stu-id="e254f-105">Starts a signature update operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e254f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e254f-106">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a><span data-ttu-id="e254f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e254f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e254f-108">*хмфандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e254f-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e254f-109">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="e254f-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="e254f-110">Обработчик для интерфейса диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="e254f-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="e254f-111">Этот маркер возвращается функцией [**мпманажеропен**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="e254f-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e254f-112">*двупдатеоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e254f-112">*dwUpdateOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e254f-113">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e254f-113">Type: **DWORD**</span></span>

<span data-ttu-id="e254f-114">Задает параметр для операции обновления сигнатур.</span><span class="sxs-lookup"><span data-stu-id="e254f-114">Specifies the option for the signature update operation.</span></span> <span data-ttu-id="e254f-115">Может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e254f-115">It can be one of the following values:</span></span>



| <span data-ttu-id="e254f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e254f-116">Value</span></span>                                                                                                                                                                                              | <span data-ttu-id="e254f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e254f-117">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <span data-ttu-id="e254f-118"><dt>**\_параметр MPUPDATE \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-118"><dt>**MPUPDATE\_OPTION\_NONE**</dt></span></span> </dl>                | <span data-ttu-id="e254f-119">Конкретный параметр не запрашивается.</span><span class="sxs-lookup"><span data-stu-id="e254f-119">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <span data-ttu-id="e254f-120"><dt>**\_параметр MPUPDATE \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-120"><dt>**MPUPDATE\_OPTION\_ASYNC**</dt></span></span> </dl>             | <span data-ttu-id="e254f-121">Операция обновления должна быть асинхронной, где **мпупдатестарт** возвращается сразу после успешного инициации обновления сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="e254f-121">The update operation is to be asynchronous, where **MpUpdateStart** returns immediately after the successful initiation of the signature update.</span></span> <span data-ttu-id="e254f-122">(По умолчанию операция обновления является синхронной, то есть **мпупдатестарт** будет возвращаться только после завершения обновления сигнатуры.)</span><span class="sxs-lookup"><span data-stu-id="e254f-122">(By default the update operation is synchronous, meaning **MpUpdateStart** will return only after the signature update is finished.)</span></span><br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <span data-ttu-id="e254f-123"><dt>**\_ \_ ход выполнения параметра MPUPDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-123"><dt>**MPUPDATE\_OPTION\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="e254f-124">Вызывающий объект заинтересован в получении сведений о ходе обновления сигнатуры с помощью обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e254f-124">The caller is interested in receiving signature update progress information via a callback.</span></span><br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <span data-ttu-id="e254f-125"><dt>**\_ \_ http-параметр MPUPDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-125"><dt>**MPUPDATE\_OPTION\_HTTP**</dt></span></span> </dl>                | <span data-ttu-id="e254f-126">Обновление сигнатур выполняется путем загрузки полного пакета сигнатур с сайта Microsoft Security Portal.</span><span class="sxs-lookup"><span data-stu-id="e254f-126">The signature update is performed by downloading the full signature package from the Microsoft security portal site.</span></span> <span data-ttu-id="e254f-127">Это можно использовать в качестве варианта отката, если клиент испытывает проблемы с загрузкой сигнатур с помощью Центр обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e254f-127">This can be used as a fallback option if the client is experiencing a signature download problem via Microsoft Update.</span></span><br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <span data-ttu-id="e254f-128"><dt>**\_UNC-параметр MPUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-128"><dt>**MPUPDATE\_OPTION\_UNC**</dt></span></span> </dl>                   | <span data-ttu-id="e254f-129">Выполняет обновление сигнатур с помощью прямого скачивания из общих UNC-папок.</span><span class="sxs-lookup"><span data-stu-id="e254f-129">Performs signature update using direct download from UNC shares.</span></span><br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <span data-ttu-id="e254f-130"><dt>**\_ \_ управляемый параметр MPUPDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-130"><dt>**MPUPDATE\_OPTION\_MANAGED**</dt></span></span> </dl>       | <span data-ttu-id="e254f-131">Выполняет обновление сигнатур с помощью управляемой службы WSUS.</span><span class="sxs-lookup"><span data-stu-id="e254f-131">Performs signature update using the Managed Service WSUS.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <span data-ttu-id="e254f-132"><dt>**\_НЕуправляемый параметр MPUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-132"><dt>**MPUPDATE\_OPTION\_UNMANAGED**</dt></span></span> </dl> | <span data-ttu-id="e254f-133">Выполняет обновление сигнатур с помощью неуправляемой службы MU/WU.</span><span class="sxs-lookup"><span data-stu-id="e254f-133">Performs signature update using the Unmanaged Service MU/WU.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="e254f-134">*пкаллбаккинфо* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e254f-134">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e254f-135">Тип: **пмпкаллбакк \_ info** .</span><span class="sxs-lookup"><span data-stu-id="e254f-135">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="e254f-136">Указатель на сведения о обратном вызове, используемые для передачи клиенту изменений состояния обновления подписи (например, запуск и завершение) и сведений о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="e254f-136">A pointer to the callback information used to feed the client with signature update state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="e254f-137">[**\_ Данные мпкаллбакк**](mpcallback-data.md) , переданные обратно в функцию обратного вызова, сообщают о фактическом состоянии обновления и сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="e254f-137">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual update state and progress-related information.</span></span> <span data-ttu-id="e254f-138">Ниже приведен список возможных обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="e254f-138">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="e254f-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e254f-139">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="e254f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e254f-140">Meaning</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <span data-ttu-id="e254f-141"><dt>**\_Начало СИГУПДАТЕ \_ мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-141"><dt>**MPNOTIFY\_SIGUPDATE\_START**</dt></span></span> </dl>                                      | <span data-ttu-id="e254f-142">Операция обновления запущена.</span><span class="sxs-lookup"><span data-stu-id="e254f-142">Update operation started.</span></span><br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <span data-ttu-id="e254f-143"><dt>**МПНОТИФИ \_ сигупдате \_ завершен**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-143"><dt>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</dt></span></span> </dl>                             | <span data-ttu-id="e254f-144">Операция обновления завершена.</span><span class="sxs-lookup"><span data-stu-id="e254f-144">Update operation completed.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <span data-ttu-id="e254f-145"><dt>**\_ \_ Начало поиска мпнотифи \_ сигупдате**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-145"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</dt></span></span> </dl>                | <span data-ttu-id="e254f-146">Поиск обновлений начат.</span><span class="sxs-lookup"><span data-stu-id="e254f-146">Search for updates started.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <span data-ttu-id="e254f-147"><dt>**\_Поиск мпнотифи \_ сигупдате \_ завершен**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-147"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</dt></span></span> </dl>       | <span data-ttu-id="e254f-148">Поиск обновлений завершен.</span><span class="sxs-lookup"><span data-stu-id="e254f-148">Search for updates completed.</span></span> <span data-ttu-id="e254f-149">Дополнительные сведения можно получить с помощью структуры [**\_ данных мпсигупдате**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e254f-149">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <span data-ttu-id="e254f-150"><dt>**\_ \_ Начало загрузки сигупдате \_ мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-150"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</dt></span></span> </dl>          | <span data-ttu-id="e254f-151">Загрузка для обновления начата.</span><span class="sxs-lookup"><span data-stu-id="e254f-151">Download for update started.</span></span><br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <span data-ttu-id="e254f-152"><dt>**\_ \_ ход загрузки сигупдате \_ мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-152"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</dt></span></span> </dl> | <span data-ttu-id="e254f-153">Сведения о ходе загрузки.</span><span class="sxs-lookup"><span data-stu-id="e254f-153">Download progress information.</span></span> <span data-ttu-id="e254f-154">Дополнительные сведения можно получить с помощью структуры [**\_ данных мпсигупдате**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e254f-154">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <span data-ttu-id="e254f-155"><dt>**\_скачивание СИГУПДАТЕ \_ мпнотифи \_ завершено**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-155"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</dt></span></span> </dl> | <span data-ttu-id="e254f-156">Загрузка для обновления завершена.</span><span class="sxs-lookup"><span data-stu-id="e254f-156">Download for update complete.</span></span> <span data-ttu-id="e254f-157">Дополнительные сведения можно получить с помощью структуры [**\_ данных мпсигупдате**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e254f-157">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <span data-ttu-id="e254f-158"><dt>**\_ \_ Запуск установки мпнотифи \_ сигупдате**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-158"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</dt></span></span> </dl>             | <span data-ttu-id="e254f-159">Установка обновления начата.</span><span class="sxs-lookup"><span data-stu-id="e254f-159">Installation of update started.</span></span><br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <span data-ttu-id="e254f-160"><dt>**\_ \_ Ход установки мпнотифи \_ сигупдате**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-160"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="e254f-161">Сведения о ходе установки.</span><span class="sxs-lookup"><span data-stu-id="e254f-161">Installation progress information.</span></span> <span data-ttu-id="e254f-162">Дополнительные сведения можно получить с помощью структуры [**\_ данных мпсигупдате**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e254f-162">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <span data-ttu-id="e254f-163"><dt>**\_Установка СИГУПДАТЕ \_ мпнотифи \_ завершена**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-163"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</dt></span></span> </dl>    | <span data-ttu-id="e254f-164">Установка обновления завершена.</span><span class="sxs-lookup"><span data-stu-id="e254f-164">Installation of update completed.</span></span> <span data-ttu-id="e254f-165">Дополнительные сведения можно получить с помощью структуры [**\_ данных мпсигупдате**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e254f-165">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <span data-ttu-id="e254f-166"><dt>**\_запрос СИГУПДАТЕ \_ мпнотифи \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-166"><dt>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</dt></span></span> </dl> | <span data-ttu-id="e254f-167">Служба защиты от вредоносных программ обработала запрос на обновление сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="e254f-167">The antimalware service processed a signature update request.</span></span> <span data-ttu-id="e254f-168">Ошибка или успех обозначается *значением hResult* в [**\_ данных мпкаллбакк**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="e254f-168">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <span data-ttu-id="e254f-169"><dt>**\_ \_ требуется перезагрузка сигупдате мпнотифи \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-169"><dt>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</dt></span></span> </dl>       | <span data-ttu-id="e254f-170">Для завершения операции обновления требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="e254f-170">Requires reboot to complete the update operation.</span></span> <span data-ttu-id="e254f-171">Ошибка или успех обозначается *значением hResult* в [**\_ данных мпкаллбакк**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="e254f-171">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="e254f-172"><dt>**\_внутренний \_ сбой мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-172"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>                                   | <span data-ttu-id="e254f-173">Операция обновления сигнатуры обнаружила общий сбой.</span><span class="sxs-lookup"><span data-stu-id="e254f-173">Signature update operation has encountered a generic failure.</span></span> <span data-ttu-id="e254f-174">Значение *hResult* в [**мпкаллбакк \_ данных**](mpcallback-data.md) имеет конкретный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e254f-174">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="e254f-175">*фупдатехандле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e254f-175">*phUpdateHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e254f-176">Тип: **пмфандле**</span><span class="sxs-lookup"><span data-stu-id="e254f-176">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="e254f-177">Возвращенный обработчик обновления, который идентифицирует инициированную в данный момент операцию обновления сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="e254f-177">Returned update handle which identifies the currently initiated signature update operation.</span></span> <span data-ttu-id="e254f-178">Этот маркер можно использовать в последующих вызовах функций, например для управления операцией обновления сигнатур.</span><span class="sxs-lookup"><span data-stu-id="e254f-178">This handle can be used in subsequent function calls, such as to control the signature update operation.</span></span> <span data-ttu-id="e254f-179">Этот маркер должен быть закрыт функцией [**мфандлеклосе**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="e254f-179">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e254f-180">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e254f-180">Return value</span></span>

<span data-ttu-id="e254f-181">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e254f-181">Type: **HRESULT**</span></span>

<span data-ttu-id="e254f-182">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="e254f-182">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="e254f-183">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e254f-183">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="e254f-184">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e254f-184">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e254f-185">Требования</span><span class="sxs-lookup"><span data-stu-id="e254f-185">Requirements</span></span>



| <span data-ttu-id="e254f-186">Требование</span><span class="sxs-lookup"><span data-stu-id="e254f-186">Requirement</span></span> | <span data-ttu-id="e254f-187">Значение</span><span class="sxs-lookup"><span data-stu-id="e254f-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e254f-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e254f-188">Minimum supported client</span></span><br/> | <span data-ttu-id="e254f-189">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e254f-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e254f-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e254f-190">Minimum supported server</span></span><br/> | <span data-ttu-id="e254f-191">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e254f-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e254f-192">Header</span><span class="sxs-lookup"><span data-stu-id="e254f-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="e254f-193"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-193"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e254f-194">DLL</span><span class="sxs-lookup"><span data-stu-id="e254f-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e254f-195"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e254f-195"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e254f-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e254f-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e254f-197">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="e254f-197">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="e254f-198">**мфандлеклосе**</span><span class="sxs-lookup"><span data-stu-id="e254f-198">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="e254f-199">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="e254f-199">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="e254f-200">**\_данные мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e254f-200">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="e254f-201">**\_данные мпсигупдате**</span><span class="sxs-lookup"><span data-stu-id="e254f-201">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> </dl>

 

 





