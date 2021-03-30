---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_AFSDBType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса сервера базы данных AFS (AFSDB).
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_AFSDBType
- DNS класса MicrosoftDNS_AFSDBType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988665"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="edf89-106">Метод Креатеинстанцефромпропертидата \_ класса Афсдбтипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="edf89-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="edf89-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса сервера базы данных AFS (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="edf89-107">The **CreateInstanceFromPropertyData** method instantiates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="edf89-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edf89-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="edf89-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="edf89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edf89-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edf89-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf89-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="edf89-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="edf89-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edf89-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf89-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="edf89-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="edf89-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edf89-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf89-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="edf89-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="edf89-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="edf89-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edf89-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="edf89-117">Class of the RR.</span></span> <span data-ttu-id="edf89-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="edf89-118">Default value is 1.</span></span> <span data-ttu-id="edf89-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="edf89-119">The following values are valid.</span></span>



| <span data-ttu-id="edf89-120">Значение</span><span class="sxs-lookup"><span data-stu-id="edf89-120">Value</span></span>                                                                                                | <span data-ttu-id="edf89-121">Значение</span><span class="sxs-lookup"><span data-stu-id="edf89-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="edf89-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="edf89-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="edf89-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="edf89-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="edf89-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="edf89-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="edf89-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="edf89-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="edf89-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="edf89-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="edf89-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="edf89-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="edf89-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="edf89-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="edf89-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="edf89-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="edf89-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="edf89-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edf89-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="edf89-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="edf89-132">*Подтип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edf89-132">*Subtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf89-133">Подтип ведущего сервера AFS.</span><span class="sxs-lookup"><span data-stu-id="edf89-133">Subtype of the host AFS server.</span></span> <span data-ttu-id="edf89-134">Для подтипа 1 (значение 1) на узле имеется сервер AFS версии 3,0 для именованной ячейки AFS.</span><span class="sxs-lookup"><span data-stu-id="edf89-134">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="edf89-135">В случае подтипа 2 (значение = 2) узел имеет прошедший проверку подлинности сервер имен, в котором размещен узел корневого каталога ячеек для именованной ячейки DCE/NCA.</span><span class="sxs-lookup"><span data-stu-id="edf89-135">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="edf89-136">*Имя сервера* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edf89-136">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf89-137">Полное доменное имя, указывающее узел с сервером для ячейки AFS, указанной в имени владельца.</span><span class="sxs-lookup"><span data-stu-id="edf89-137">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="edf89-138">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="edf89-138">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="edf89-139">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="edf89-139">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edf89-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edf89-140">Return value</span></span>

<span data-ttu-id="edf89-141">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="edf89-141">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="edf89-142">Требования</span><span class="sxs-lookup"><span data-stu-id="edf89-142">Requirements</span></span>



| <span data-ttu-id="edf89-143">Требование</span><span class="sxs-lookup"><span data-stu-id="edf89-143">Requirement</span></span> | <span data-ttu-id="edf89-144">Значение</span><span class="sxs-lookup"><span data-stu-id="edf89-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edf89-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edf89-145">Minimum supported client</span></span><br/> | <span data-ttu-id="edf89-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="edf89-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="edf89-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edf89-147">Minimum supported server</span></span><br/> | <span data-ttu-id="edf89-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="edf89-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="edf89-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="edf89-149">Namespace</span></span><br/>                | <span data-ttu-id="edf89-150">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="edf89-150">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="edf89-151">MOF</span><span class="sxs-lookup"><span data-stu-id="edf89-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edf89-152"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edf89-152"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edf89-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edf89-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf89-154">**Микрософтднс \_ афсдбтипе**</span><span class="sxs-lookup"><span data-stu-id="edf89-154">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="edf89-155">**Метод Modify \_ класса микрософтднс афсдбтипе**</span><span class="sxs-lookup"><span data-stu-id="edf89-155">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="edf89-156">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="edf89-156">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





