---
title: Метод Modify класса MicrosoftDNS_WINSRType
description: Метод Modify обновляет запись ресурса WINSR (WINSR) для просмотра WINS.
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_WINSRType класс
- MicrosoftDNS_WINSRType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137402"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="90946-106">Метод Modify \_ класса микрософтднс винсртипе</span><span class="sxs-lookup"><span data-stu-id="90946-106">Modify method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="90946-107">Метод **Modify** обновляет запись ресурса WINSR (WINSR) для просмотра WINS.</span><span class="sxs-lookup"><span data-stu-id="90946-107">The **Modify** method updates a WINS Reverse Look up (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="90946-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90946-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="90946-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90946-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90946-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="90946-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90946-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="90946-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="90946-112">*Маппингфлаг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="90946-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90946-113">Флаг сопоставления WINSR, указывающий, следует ли включать запись в репликацию зоны.</span><span class="sxs-lookup"><span data-stu-id="90946-113">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="90946-114">Он может иметь только два значения: 0x80000000 и 0x00010000, соответствующие флагам репликации и без репликации (локальная запись) соответственно.</span><span class="sxs-lookup"><span data-stu-id="90946-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="90946-115">*Лукуптимеаут* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="90946-115">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90946-116">Время ожидания (в секундах) для DNS-сервера, использующего обратный поиск WINS.</span><span class="sxs-lookup"><span data-stu-id="90946-116">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="90946-117">*CacheTimeout* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="90946-117">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90946-118">Время (в секундах), в течение которого DNS-сервер, использующий поиск WINS, может кэшировать ответ WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="90946-118">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="90946-119">*Ресултдомаин* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="90946-119">*ResultDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90946-120">Имя домена, добавляемое к возвращенным NetBIOS-именам.</span><span class="sxs-lookup"><span data-stu-id="90946-120">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="90946-121">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="90946-121">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="90946-122">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="90946-122">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90946-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90946-123">Return value</span></span>

<span data-ttu-id="90946-124">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="90946-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90946-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90946-125">Remarks</span></span>

<span data-ttu-id="90946-126">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="90946-126">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="90946-127">Требования</span><span class="sxs-lookup"><span data-stu-id="90946-127">Requirements</span></span>



| <span data-ttu-id="90946-128">Требование</span><span class="sxs-lookup"><span data-stu-id="90946-128">Requirement</span></span> | <span data-ttu-id="90946-129">Значение</span><span class="sxs-lookup"><span data-stu-id="90946-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90946-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90946-130">Minimum supported client</span></span><br/> | <span data-ttu-id="90946-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="90946-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="90946-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90946-132">Minimum supported server</span></span><br/> | <span data-ttu-id="90946-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="90946-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="90946-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="90946-134">Namespace</span></span><br/>                | <span data-ttu-id="90946-135">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="90946-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="90946-136">MOF</span><span class="sxs-lookup"><span data-stu-id="90946-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90946-137"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90946-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90946-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90946-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90946-139">**Микрософтднс \_ винсртипе**</span><span class="sxs-lookup"><span data-stu-id="90946-139">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="90946-140">**Метод Креатеинстанцефромпропертидата \_ класса Винсртипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="90946-140">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="90946-141">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="90946-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





