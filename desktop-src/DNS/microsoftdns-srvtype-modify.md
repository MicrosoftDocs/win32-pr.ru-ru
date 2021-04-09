---
title: Метод Modify класса MicrosoftDNS_SRVType
description: Метод Modify обновляет запись ресурса службы (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_SRVType класс
- MicrosoftDNS_SRVType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071955"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="38aa9-106">Метод Modify \_ класса микрософтднс срвтипе</span><span class="sxs-lookup"><span data-stu-id="38aa9-106">Modify method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="38aa9-107">Метод **Modify** обновляет запись ресурса службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="38aa9-107">The **Modify** method updates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="38aa9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38aa9-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="38aa9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="38aa9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38aa9-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="38aa9-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38aa9-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="38aa9-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="38aa9-112">*Приоритет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="38aa9-112">*Priority* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38aa9-113">Приоритет целевого узла, указанного в имени владельца.</span><span class="sxs-lookup"><span data-stu-id="38aa9-113">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="38aa9-114">Более низкие значения подразумевают более высокие приоритеты.</span><span class="sxs-lookup"><span data-stu-id="38aa9-114">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="38aa9-115">*Вес* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="38aa9-115">*Weight* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38aa9-116">Вес целевого узла.</span><span class="sxs-lookup"><span data-stu-id="38aa9-116">Weight of the target host.</span></span> <span data-ttu-id="38aa9-117">Это полезно при выборе между узлами с одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="38aa9-117">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="38aa9-118">Вероятность использования этого узла должна быть пропорциональна его весу.</span><span class="sxs-lookup"><span data-stu-id="38aa9-118">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="38aa9-119">*Порт* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="38aa9-119">*Port* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38aa9-120">Порт, используемый на целевом узле службы протокола.</span><span class="sxs-lookup"><span data-stu-id="38aa9-120">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="38aa9-121">*Срвдомаиннаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="38aa9-121">*SRVDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38aa9-122">Полное доменное имя целевого узла.</span><span class="sxs-lookup"><span data-stu-id="38aa9-122">FQDN of the target host.</span></span> <span data-ttu-id="38aa9-123">Целевой объект \\ . \\ означает, что служба не будет доступна в этом домене.</span><span class="sxs-lookup"><span data-stu-id="38aa9-123">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="38aa9-124">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="38aa9-124">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="38aa9-125">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="38aa9-125">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38aa9-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38aa9-126">Return value</span></span>

<span data-ttu-id="38aa9-127">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="38aa9-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38aa9-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38aa9-128">Remarks</span></span>

<span data-ttu-id="38aa9-129">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="38aa9-129">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="38aa9-130">Требования</span><span class="sxs-lookup"><span data-stu-id="38aa9-130">Requirements</span></span>



| <span data-ttu-id="38aa9-131">Требование</span><span class="sxs-lookup"><span data-stu-id="38aa9-131">Requirement</span></span> | <span data-ttu-id="38aa9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="38aa9-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38aa9-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38aa9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="38aa9-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="38aa9-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="38aa9-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38aa9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="38aa9-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38aa9-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="38aa9-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38aa9-137">Namespace</span></span><br/>                | <span data-ttu-id="38aa9-138">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="38aa9-138">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="38aa9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="38aa9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38aa9-140"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38aa9-140"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38aa9-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38aa9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38aa9-142">**Микрософтднс \_ срвтипе**</span><span class="sxs-lookup"><span data-stu-id="38aa9-142">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="38aa9-143">**Метод Креатеинстанцефромпропертидата \_ класса Срвтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="38aa9-143">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="38aa9-144">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="38aa9-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





