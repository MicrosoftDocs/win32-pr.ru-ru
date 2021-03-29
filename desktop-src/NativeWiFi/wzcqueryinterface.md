---
description: Предоставляет подробные сведения для интерфейса беспроводной локальной сети, управляемого службой настройки беспроводной связи.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Функция Взккуеринтерфаце (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912520"
---
# <a name="wzcqueryinterface-function"></a><span data-ttu-id="14447-103">Функция Взккуеринтерфаце</span><span class="sxs-lookup"><span data-stu-id="14447-103">WZCQueryInterface function</span></span>

<span data-ttu-id="14447-104">\[**Взккуеринтерфаце** больше не поддерживается в Windows Vista и windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="14447-104">\[**WZCQueryInterface** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="14447-105">Вместо этого используйте функцию [**вланкуеринтерфаце**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) .</span><span class="sxs-lookup"><span data-stu-id="14447-105">Use the [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) function instead.</span></span> <span data-ttu-id="14447-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).</span><span class="sxs-lookup"><span data-stu-id="14447-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).</span></span> <span data-ttu-id="14447-107">\]</span><span class="sxs-lookup"><span data-stu-id="14447-107">\]</span></span>

<span data-ttu-id="14447-108">Функция **взккуеринтерфаце** предоставляет подробные сведения для интерфейса беспроводной локальной сети, управляемого службой настройки беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="14447-108">The **WZCQueryInterface** function provides detailed information for a wireless LAN interface managed by the Wireless Zero Configuration service.</span></span>

<span data-ttu-id="14447-109">Предоставляет подробные сведения для данного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14447-109">Provides detailed information for a given interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="14447-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14447-110">Syntax</span></span>


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="14447-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="14447-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14447-112">*псрваддр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14447-112">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14447-113">Указатель на строку, содержащую имя компьютера, на котором должна быть выполнена эта функция.</span><span class="sxs-lookup"><span data-stu-id="14447-113">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="14447-114">Если этот параметр имеет **значение NULL**, то на локальном компьютере будет выполнен запрос к службе настройки беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="14447-114">If this parameter is **NULL**, then the Wireless Zero Configuration service is queried on the local computer.</span></span>

<span data-ttu-id="14447-115">Если указанный параметр *псрваддр* является удаленным компьютером, удаленный компьютер должен поддерживать удаленные вызовы RPC.</span><span class="sxs-lookup"><span data-stu-id="14447-115">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="14447-116">*двинфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14447-116">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14447-117">Поля для запроса.</span><span class="sxs-lookup"><span data-stu-id="14447-117">The fields to be queried.</span></span> <span data-ttu-id="14447-118">Это битовая маска, которая может содержать любое сочетание следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="14447-118">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="14447-119">Значение</span><span class="sxs-lookup"><span data-stu-id="14447-119">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="14447-120">Значение</span><span class="sxs-lookup"><span data-stu-id="14447-120">Meaning</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <span data-ttu-id="14447-121"><dt>**Intf \_ ДИНФЛАГС**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="14447-121"><dt>**INTF\_DYNFLAGS**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="14447-122">Возвращает значение для элемента **двдинфлагс** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-122">Return the value for the **dwDynFlags** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="14447-123"><dt>**Intf \_ DESCR**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-123"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>                      | <span data-ttu-id="14447-124">Возвращает значение для элемента **всздескр** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-124">Return the value for the **wszDescr** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="14447-125"><dt>**Intf \_ НДИСМЕДИА**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-125"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="14447-126">Возвращает значения для элементов **улмедиастате**, **улмедиатипе** и **улфисикалмедиатипе** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-126">Return the values for the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <span data-ttu-id="14447-127"><dt>**Intf \_ ПРЕФЛИСТ**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-127"><dt>**INTF\_PREFLIST**</dt> <dt>0x00040000</dt></span></span> </dl>             | <span data-ttu-id="14447-128">Возвращает предпочтительный список сетей в элементе **рдстссидлист** структуры [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-128">Return the preferred list of networks in the **rdStSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <span data-ttu-id="14447-129"><dt>**Intf \_ ВОЗМОЖНОСТИ**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-129"><dt>**INTF\_CAPABILITIES**</dt> <dt>0x00080000</dt></span></span> </dl> | <span data-ttu-id="14447-130">Возвращает значения для элементов **двкапабилитиес** и **рдниккапабилитиес** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-130">Return the values for the **dwCapabilities** and the **rdNicCapabilities** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <span data-ttu-id="14447-131"><dt>**Intf \_ ИНФРАМОДЕ**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-131"><dt>**INTF\_INFRAMODE**</dt> <dt>0x00200000</dt></span></span> </dl>          | <span data-ttu-id="14447-132">Возвращает значение для элемента **нинфрамоде** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-132">Return the value for the **nInfraMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="14447-133">Элемент **нинфрамоде** допустим только в некоторых состояниях контекста интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14447-133">The **nInfraMode** member is valid only in some interface context states.</span></span><br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <span data-ttu-id="14447-134"><dt>**Intf \_ АУСМОДЕ**</dt> <dt>0x00400000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-134"><dt>**INTF\_AUTHMODE**</dt> <dt>0x00400000</dt></span></span> </dl>             | <span data-ttu-id="14447-135">Возвращает значение для элемента **наусмоде** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-135">Return the value for the **nAuthMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="14447-136">Элемент **наусмоде** допустим только в некоторых состояниях контекста интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14447-136">The **nAuthMode** member is valid only in some interface context states.</span></span><br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <span data-ttu-id="14447-137"><dt>**Intf \_ ВЕПСТАТУС**</dt> <dt>0x00800000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-137"><dt>**INTF\_WEPSTATUS**</dt> <dt>0x00800000</dt></span></span> </dl>          | <span data-ttu-id="14447-138">Возвращает значение для элемента **нвепстатус** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-138">Return the value for the **nWepStatus** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="14447-139">Элемент **нвепстатус** допустим только в некоторых состояниях контекста интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14447-139">The **nWepStatus** member is valid only in some interface context states.</span></span><br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <span data-ttu-id="14447-140"><dt>**Intf \_ SSID**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-140"><dt>**INTF\_SSID**</dt> <dt>0x01000000</dt></span></span> </dl>                         | <span data-ttu-id="14447-141">Возвращает значение для элемента **рдссид** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-141">Return the value for the **rdSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="14447-142">Элемент **рдссид** допустим только в некоторых состояниях контекста интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14447-142">The **rdSSID** member is valid only in some interface context states.</span></span><br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <span data-ttu-id="14447-143"><dt>**Intf \_ BSSID**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-143"><dt>**INTF\_BSSID**</dt> <dt>0x02000000</dt></span></span> </dl>                      | <span data-ttu-id="14447-144">Возвращает значение для элемента **рдбссид** в структуре [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-144">Return the value for the **rdBSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="14447-145">Элемент **рдбссид** допустим только в некоторых состояниях контекста интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14447-145">The **rdBSSID** member is valid only in some interface context states.</span></span><br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <span data-ttu-id="14447-146"><dt>**Intf \_ БССИДЛИСТ**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="14447-146"><dt>**INTF\_BSSIDLIST**</dt> <dt>0x04000000</dt></span></span> </dl>          | <span data-ttu-id="14447-147">Возврат видимого списка сетей в элементе **рдбссидлист** структуры [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-147">Return the visible list of networks in the **rdBSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="14447-148">Элемент **рдбссидлист** допустим только в некоторых состояниях контекста интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14447-148">The **rdBSSIDList** member is valid only in some interface context states.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="14447-149">*пинтф* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="14447-149">*pIntf* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14447-150">На входе — указатель на ключ интерфейса для запроса.</span><span class="sxs-lookup"><span data-stu-id="14447-150">On input, a pointer to the key of the interface to query.</span></span> <span data-ttu-id="14447-151">На выходе — указатель на запрошенные данные интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14447-151">On output, a pointer to the requested interface data.</span></span> <span data-ttu-id="14447-152">Этот параметр является указателем на структуру [**\_ записи intf**](intf-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="14447-152">This parameter is a pointer to an [**INTF\_ENTRY**](intf-entry.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="14447-153">*пдваутфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="14447-153">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14447-154">Набор полей, успешно извлеченных.</span><span class="sxs-lookup"><span data-stu-id="14447-154">A set of fields successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14447-155">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14447-155">Return value</span></span>

<span data-ttu-id="14447-156">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="14447-156">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="14447-157">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="14447-157">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="14447-158">Код возврата</span><span class="sxs-lookup"><span data-stu-id="14447-158">Return code</span></span>                                                                                               | <span data-ttu-id="14447-159">Описание</span><span class="sxs-lookup"><span data-stu-id="14447-159">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14447-160"><dt>**некоторая ошибка в \_ \_ корзине**</dt></span><span class="sxs-lookup"><span data-stu-id="14447-160"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="14447-161">Блоки управления хранилищем были уничтожены.</span><span class="sxs-lookup"><span data-stu-id="14447-161">The storage control blocks were destroyed.</span></span> <span data-ttu-id="14447-162">Эта ошибка возвращается, если служба настройки беспроводной связи не инициализирует внутренние объекты.</span><span class="sxs-lookup"><span data-stu-id="14447-162">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="14447-163"><dt>**\_файл ошибок \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="14447-163"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="14447-164">Системе не удается найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="14447-164">The system cannot find the file specified.</span></span> <span data-ttu-id="14447-165">Эта ошибка возвращается, если идентификатор GUID в элементе **всзгуид** структуры [**\_ записи intf**](intf-entry.md) , на который указывает параметр *пинтф* , не соответствует ни одному из интерфейсов беспроводной локальной сети на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="14447-165">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="14447-166"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="14447-166"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="14447-167">Неверный параметр.</span><span class="sxs-lookup"><span data-stu-id="14447-167">A parameter is incorrect.</span></span> <span data-ttu-id="14447-168">Эта ошибка возвращается, если параметр *пинтф* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="14447-168">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="14447-169">Эта ошибка возвращается, если элемент **всзгуид** структуры [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* , имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="14447-169">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="14447-170"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="14447-170"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="14447-171">Недостаточно памяти для обработки этого запроса и выделения памяти для результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="14447-171">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="14447-172"><dt>**\_Состояние RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="14447-172"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="14447-173">Различные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="14447-173">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="14447-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14447-174">Remarks</span></span>

<span data-ttu-id="14447-175">Элемент **всзгуид** структуры [**\_ записи intf**](intf-entry.md) , на который указывает параметр *пинтф* , должен содержать идентификатор GUID интерфейса для беспроводных локальных сетей.</span><span class="sxs-lookup"><span data-stu-id="14447-175">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="14447-176">Список интерфейсов беспроводной локальной сети можно получить, вызвав функцию [**взценуминтерфацес**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="14447-176">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

<span data-ttu-id="14447-177">Следующие члены структуры [**\_ записи intf**](intf-entry.md) , на которую указывает *пинтф* , должны иметь значение 0 перед вызовом функции **взккуеринтерфаце** : **Рдссид**, **рдбссид**, **рдбссидлист**, **рдстссидлист** и **рдктрлдата**.</span><span class="sxs-lookup"><span data-stu-id="14447-177">The following members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* must be set to 0 before a call to the **WZCQueryInterface** function: **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData**.</span></span>

<span data-ttu-id="14447-178">Служба настройки беспроводной связи не аутомотикалли обновление состояния носителя, даже если получены подключения к мультимедиа и отключенные события.</span><span class="sxs-lookup"><span data-stu-id="14447-178">The Wireless Zero Configuration service does not automotically update media state, even when media connected and disconnected events are received.</span></span> <span data-ttu-id="14447-179">Приложение должно принудительно обновить состояние носителя, вызвав функцию [**взкрефрешинтерфаце**](wzcrefreshinterface.md) перед вызовом функции **взккуеринтерфаце** , если требуется запросить состояние носителя NDIS (в \_ параметре *двинфлагс* будет задан бит intf ндисмедиа).</span><span class="sxs-lookup"><span data-stu-id="14447-179">An application should force a media state refresh by calling the [**WZCRefreshInterface**](wzcrefreshinterface.md) function before calling the **WZCQueryInterface** function if the NDIS media state is to be requested (the INTF\_NDISMEDIA bit will be set in the *dwInFlags* parameter).</span></span>

<span data-ttu-id="14447-180">Если параметр *двинфлагс* содержит **intf \_ бссидлист**, функция **взккуеринтерфаце** не устанавливает дваутфлагс с **intf \_** бссидлист *, если* видимый список сетей пуст.</span><span class="sxs-lookup"><span data-stu-id="14447-180">When the *dwInFlags* parameter contains **INTF\_BSSIDLIST**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_BSSIDLIST** if the visible list of networks is empty.</span></span> <span data-ttu-id="14447-181">Если параметр *двинфлагс* содержит **intf \_ SSID**, функция **взккуеринтерфаце** не устанавливает *дваутфлагс* с **intf \_ SSID** , если SSID недоступен.</span><span class="sxs-lookup"><span data-stu-id="14447-181">When the *dwInFlags* parameter contains **INTF\_SSID**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_SSID** if no SSID is available.</span></span>

<span data-ttu-id="14447-182">Если функция **взккуеринтерфаце** возвращает ошибку \_ успешного выполнения, вызывающий объект должен вызвать функцию [**функции LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) с параметром *пинтф* , чтобы освободить внутренние буферы, выделенные для данных, возвращаемых после того, как эти сведения больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="14447-182">If the **WZCQueryInterface** function returns ERROR\_SUCCESS, the caller should call the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function with the *pIntf* parameter to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span> <span data-ttu-id="14447-183">Это освобождает буферы, используемые членами **рдссид**, **рдбссид**, **рдбссидлист**, **рдстссидлист** и **рдктрлдата** в структуре [**\_ записи intf**](intf-entry.md) , на которые указывает параметр *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="14447-183">This releases the buffers used by the **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="14447-184">Файл заголовка *взксапи. h* и файл библиотеки импорта *взксапи. lib* недоступны в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="14447-184">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14447-185">Требования</span><span class="sxs-lookup"><span data-stu-id="14447-185">Requirements</span></span>



| <span data-ttu-id="14447-186">Требование</span><span class="sxs-lookup"><span data-stu-id="14447-186">Requirement</span></span> | <span data-ttu-id="14447-187">Значение</span><span class="sxs-lookup"><span data-stu-id="14447-187">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14447-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14447-188">Minimum supported client</span></span><br/> | <span data-ttu-id="14447-189">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="14447-189">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14447-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14447-190">Minimum supported server</span></span><br/> | <span data-ttu-id="14447-191">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14447-191">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14447-192">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="14447-192">End of client support</span></span><br/>    | <span data-ttu-id="14447-193">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="14447-193">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="14447-194">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="14447-194">End of server support</span></span><br/>    | <span data-ttu-id="14447-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14447-195">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="14447-196">Header</span><span class="sxs-lookup"><span data-stu-id="14447-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="14447-197"><dt>Взксапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="14447-197"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="14447-198">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14447-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="14447-199"><dt>Взксапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14447-199"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="14447-200">DLL</span><span class="sxs-lookup"><span data-stu-id="14447-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14447-201"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14447-201"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14447-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14447-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14447-203">**\_запись intf**</span><span class="sxs-lookup"><span data-stu-id="14447-203">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> <dt>

[<span data-ttu-id="14447-204">**взцеаполжетинтерфацепарамс**</span><span class="sxs-lookup"><span data-stu-id="14447-204">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="14447-205">**взценуминтерфацес**</span><span class="sxs-lookup"><span data-stu-id="14447-205">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="14447-206">**взкрефрешинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="14447-206">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
