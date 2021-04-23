---
title: Структура MPSIGUPDATE_DATA (Мпклиент. h)
description: Данные уведомления, передаваемые функции обратного вызова обновления сигнатур.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA структуры устаревшие функции среды Windows
- Функции PMPSIGUPDATE_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136471"
---
# <a name="mpsigupdate_data-structure"></a><span data-ttu-id="998b1-105">\_Структура данных мпсигупдате</span><span class="sxs-lookup"><span data-stu-id="998b1-105">MPSIGUPDATE\_DATA structure</span></span>

<span data-ttu-id="998b1-106">Данные уведомления, передаваемые функции обратного вызова обновления сигнатур.</span><span class="sxs-lookup"><span data-stu-id="998b1-106">Notification data passed to the signature update callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="998b1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="998b1-107">Syntax</span></span>


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a><span data-ttu-id="998b1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="998b1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="998b1-109">**двперценткомплете**</span><span class="sxs-lookup"><span data-stu-id="998b1-109">**dwPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="998b1-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="998b1-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="998b1-111">Оценка процента между всеми обновлениями, которые были загружены и (или) установлены.</span><span class="sxs-lookup"><span data-stu-id="998b1-111">An estimate of the percentage across all the updates that have been downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="998b1-112">**двтоталупдатес**</span><span class="sxs-lookup"><span data-stu-id="998b1-112">**dwTotalUpdates**</span></span>
</dt> <dd>

<span data-ttu-id="998b1-113">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="998b1-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="998b1-114">Общее число обновлений для скачивания и (или) установки.</span><span class="sxs-lookup"><span data-stu-id="998b1-114">Total number of updates to download and/or install.</span></span>

</dd> <dt>

<span data-ttu-id="998b1-115">**двкуррентупдатеиндекс**</span><span class="sxs-lookup"><span data-stu-id="998b1-115">**dwCurrentUpdateIndex**</span></span>
</dt> <dd>

<span data-ttu-id="998b1-116">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="998b1-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="998b1-117">Значение индекса, начинающееся с нуля, которое указывает, какое обновление в данный момент должно быть загружено и (или) установлено.</span><span class="sxs-lookup"><span data-stu-id="998b1-117">Zero-based index value that specifies which update among those required is currently being downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="998b1-118">**eType**</span><span class="sxs-lookup"><span data-stu-id="998b1-118">**eType**</span></span>
</dt> <dd>

<span data-ttu-id="998b1-119">Тип: **мпсигупдате \_ тип**</span><span class="sxs-lookup"><span data-stu-id="998b1-119">Type: **MPSIGUPDATE\_TYPE**</span></span>

</dd> <dd>

<span data-ttu-id="998b1-120">Тип обновления.</span><span class="sxs-lookup"><span data-stu-id="998b1-120">Update type.</span></span> <span data-ttu-id="998b1-121">Одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="998b1-121">One of the following possible values:</span></span>



| <span data-ttu-id="998b1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="998b1-122">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="998b1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="998b1-123">Meaning</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <span data-ttu-id="998b1-124"><dt>**\_тип мпсигупдате \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-124"><dt>**MPSIGUPDATE\_TYPE\_NONE**</dt></span></span> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <span data-ttu-id="998b1-125"><dt>**\_ \_ управляемый тип мпсигупдате**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-125"><dt>**MPSIGUPDATE\_TYPE\_MANAGED**</dt></span></span> </dl>                                   | <span data-ttu-id="998b1-126">Обновление WSUS.</span><span class="sxs-lookup"><span data-stu-id="998b1-126">WSUS update.</span></span> <span data-ttu-id="998b1-127">Для отмены требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="998b1-127">Cancel requires administrator rights.</span></span><br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <span data-ttu-id="998b1-128"><dt>**МПСИГУПДАТЕ \_ тип \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-128"><dt>**MPSIGUPDATE\_TYPE\_HTTP**</dt></span></span> </dl>                                            | <span data-ttu-id="998b1-129">Обновление HTTP.</span><span class="sxs-lookup"><span data-stu-id="998b1-129">HTTP update.</span></span> <span data-ttu-id="998b1-130">Права администратора, которые не требуются для отмены.</span><span class="sxs-lookup"><span data-stu-id="998b1-130">Administrator rights not needed to cancel.</span></span><br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <span data-ttu-id="998b1-131"><dt>**МПСИГУПДАТЕ \_ тип \_ HTTP \_ SRV**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-131"><dt>**MPSIGUPDATE\_TYPE\_HTTP\_SRV**</dt></span></span> </dl>                               | <span data-ttu-id="998b1-132">HTTP из службы.</span><span class="sxs-lookup"><span data-stu-id="998b1-132">HTTP from service.</span></span> <span data-ttu-id="998b1-133">Для отмены требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="998b1-133">Cancel requires administrator rights.</span></span><br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <span data-ttu-id="998b1-134"><dt>**МПСИГУПДАТЕ \_ типа \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-134"><dt>**MPSIGUPDATE\_TYPE\_UNC**</dt></span></span> </dl>                                               | <span data-ttu-id="998b1-135">Общий UNC-ресурс.</span><span class="sxs-lookup"><span data-stu-id="998b1-135">UNC share.</span></span> <span data-ttu-id="998b1-136">Права администратора, которые не требуются для отмены.</span><span class="sxs-lookup"><span data-stu-id="998b1-136">Administrator rights not needed to cancel.</span></span><br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <span data-ttu-id="998b1-137"><dt>**\_НЕуправляемый тип мпсигупдате \_**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-137"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED**</dt></span></span> </dl>                             | <span data-ttu-id="998b1-138">Обновление MU/WU.</span><span class="sxs-lookup"><span data-stu-id="998b1-138">MU/WU update.</span></span> <span data-ttu-id="998b1-139">Для отмены требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="998b1-139">Cancel requires administrator rights.</span></span><br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <span data-ttu-id="998b1-140"><dt>**\_ \_ управляемая платформа типа мпсигупдате \_**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-140"><dt>**MPSIGUPDATE\_TYPE\_MANAGED\_PLATFORM**</dt></span></span> </dl>       | <span data-ttu-id="998b1-141">Обновление WSUS для платформы.</span><span class="sxs-lookup"><span data-stu-id="998b1-141">WSUS update for PLATFORM.</span></span> <span data-ttu-id="998b1-142">Для отмены требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="998b1-142">Cancel requires administrator rights.</span></span><br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <span data-ttu-id="998b1-143"><dt>**\_ \_ неуправляемая платформа типа \_ мпсигупдате**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-143"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED\_PLATFORM**</dt></span></span> </dl> | <span data-ttu-id="998b1-144">Обновление MU/WU для платформы.</span><span class="sxs-lookup"><span data-stu-id="998b1-144">MU/WU update for PLATFORM.</span></span> <span data-ttu-id="998b1-145">Для отмены требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="998b1-145">Cancel requires administrator rights.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="998b1-146">**Этап**</span><span class="sxs-lookup"><span data-stu-id="998b1-146">**Stage**</span></span>
</dt> <dd>

<span data-ttu-id="998b1-147">Тип: **\_ \_ этап обновления пакета управления**</span><span class="sxs-lookup"><span data-stu-id="998b1-147">Type: **MP\_UPDATE\_STAGE**</span></span>

</dd> <dd>

<span data-ttu-id="998b1-148">Стадия обновления.</span><span class="sxs-lookup"><span data-stu-id="998b1-148">Update stage.</span></span> <span data-ttu-id="998b1-149">Одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="998b1-149">One of the following possible values:</span></span>



| <span data-ttu-id="998b1-150">Значение</span><span class="sxs-lookup"><span data-stu-id="998b1-150">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="998b1-151">Значение</span><span class="sxs-lookup"><span data-stu-id="998b1-151">Meaning</span></span>                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <span data-ttu-id="998b1-152"><dt>**\_неизвестная стадия пакета управления \_**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-152"><dt>**MP\_STAGE\_UNKNOWN**</dt></span></span> </dl>       | <span data-ttu-id="998b1-153">Неизвестный этап обновления.</span><span class="sxs-lookup"><span data-stu-id="998b1-153">Update stage unknown.</span></span><br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <span data-ttu-id="998b1-154"><dt>**\_Обновление поиска \_ MP**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-154"><dt>**MP\_SEARCH\_UPDATE**</dt></span></span> </dl>       | <span data-ttu-id="998b1-155">Обновление этапа поиска.</span><span class="sxs-lookup"><span data-stu-id="998b1-155">Update search stage.</span></span><br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <span data-ttu-id="998b1-156"><dt>**\_обновление загрузки пакета управления \_**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-156"><dt>**MP\_DOWNLOAD\_UPDATE**</dt></span></span> </dl> | <span data-ttu-id="998b1-157">Стадия скачивания обновлений.</span><span class="sxs-lookup"><span data-stu-id="998b1-157">Update download stage.</span></span><br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <span data-ttu-id="998b1-158"><dt>**\_Установка \_ обновления MP**</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-158"><dt>**MP\_INSTALL\_UPDATE**</dt></span></span> </dl>    | <span data-ttu-id="998b1-159">Обновление этапа установки.</span><span class="sxs-lookup"><span data-stu-id="998b1-159">Update install stage.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="998b1-160">**Путь**</span><span class="sxs-lookup"><span data-stu-id="998b1-160">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="998b1-161">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="998b1-161">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="998b1-162">Путь обновления.</span><span class="sxs-lookup"><span data-stu-id="998b1-162">Update path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="998b1-163">Требования</span><span class="sxs-lookup"><span data-stu-id="998b1-163">Requirements</span></span>



| <span data-ttu-id="998b1-164">Требование</span><span class="sxs-lookup"><span data-stu-id="998b1-164">Requirement</span></span> | <span data-ttu-id="998b1-165">Значение</span><span class="sxs-lookup"><span data-stu-id="998b1-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="998b1-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="998b1-166">Minimum supported client</span></span><br/> | <span data-ttu-id="998b1-167">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="998b1-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="998b1-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="998b1-168">Minimum supported server</span></span><br/> | <span data-ttu-id="998b1-169">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="998b1-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="998b1-170">Header</span><span class="sxs-lookup"><span data-stu-id="998b1-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="998b1-171"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="998b1-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





