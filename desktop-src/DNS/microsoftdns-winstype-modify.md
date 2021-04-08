---
title: Метод Modify класса MicrosoftDNS_WINSType
description: Метод Modify обновляет запись ресурса службы Windows Internet Name Service (WINS).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_WINSType класс
- MicrosoftDNS_WINSType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892218"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="5eabc-106">Метод Modify \_ класса микрософтднс винстипе</span><span class="sxs-lookup"><span data-stu-id="5eabc-106">Modify method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="5eabc-107">Метод **Modify** обновляет запись ресурса службы Windows Internet Name Service (WINS).</span><span class="sxs-lookup"><span data-stu-id="5eabc-107">The **Modify** method updates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eabc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5eabc-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5eabc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5eabc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eabc-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5eabc-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5eabc-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="5eabc-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="5eabc-112">*Маппингфлаг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5eabc-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5eabc-113">Флаг сопоставления WINS, указывающий, следует ли включать запись в репликацию зоны.</span><span class="sxs-lookup"><span data-stu-id="5eabc-113">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="5eabc-114">Он может иметь только два значения: 0x80000000 и 0x00010000, соответствующие флагам репликации и без репликации (локальная запись) соответственно.</span><span class="sxs-lookup"><span data-stu-id="5eabc-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="5eabc-115">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="5eabc-115">The following values are valid.</span></span>



| <span data-ttu-id="5eabc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5eabc-116">Value</span></span>                                                                                                                                               | <span data-ttu-id="5eabc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5eabc-117">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="5eabc-118"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="5eabc-118"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="5eabc-119">Флаг репликации</span><span class="sxs-lookup"><span data-stu-id="5eabc-119">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="5eabc-120"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="5eabc-120"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="5eabc-121">Флаг отсутствия репликации (локальная запись)</span><span class="sxs-lookup"><span data-stu-id="5eabc-121">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5eabc-122">*Лукуптимеаут* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5eabc-122">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5eabc-123">Время в секундах, в течение которого DNS-сервер пытается выполнить разрешение с помощью поиска WINS.</span><span class="sxs-lookup"><span data-stu-id="5eabc-123">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="5eabc-124">*CacheTimeout* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5eabc-124">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5eabc-125">Время в секундах, в течение которого DNS-сервер, использующий поиск WINS, может кэшировать ответ WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="5eabc-125">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="5eabc-126">*Винссерверс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5eabc-126">*WinsServers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5eabc-127">Список разделенных запятыми IP-адресов WINS-серверов, используемых при поиске WINS.</span><span class="sxs-lookup"><span data-stu-id="5eabc-127">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="5eabc-128">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="5eabc-128">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5eabc-129">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="5eabc-129">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eabc-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5eabc-130">Return value</span></span>

<span data-ttu-id="5eabc-131">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5eabc-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eabc-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5eabc-132">Remarks</span></span>

<span data-ttu-id="5eabc-133">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="5eabc-133">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eabc-134">Требования</span><span class="sxs-lookup"><span data-stu-id="5eabc-134">Requirements</span></span>



| <span data-ttu-id="5eabc-135">Требование</span><span class="sxs-lookup"><span data-stu-id="5eabc-135">Requirement</span></span> | <span data-ttu-id="5eabc-136">Значение</span><span class="sxs-lookup"><span data-stu-id="5eabc-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5eabc-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5eabc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5eabc-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5eabc-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5eabc-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5eabc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5eabc-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5eabc-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5eabc-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5eabc-141">Namespace</span></span><br/>                | <span data-ttu-id="5eabc-142">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="5eabc-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5eabc-143">MOF</span><span class="sxs-lookup"><span data-stu-id="5eabc-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5eabc-144"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5eabc-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eabc-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5eabc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eabc-146">**Микрософтднс \_ винстипе**</span><span class="sxs-lookup"><span data-stu-id="5eabc-146">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="5eabc-147">**Метод Креатеинстанцефромпропертидата \_ класса Винстипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="5eabc-147">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5eabc-148">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="5eabc-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





