---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MINFOType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса почтовых сведений (MINFO).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MINFOType
- DNS класса MicrosoftDNS_MINFOType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a565b1575dc51a59a09faea6fd271d719518f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071152"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="04f6e-106">Метод Креатеинстанцефромпропертидата \_ класса Минфотипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="04f6e-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="04f6e-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса почтовых сведений (MINFO).</span><span class="sxs-lookup"><span data-stu-id="04f6e-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f6e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04f6e-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="04f6e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="04f6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f6e-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f6e-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="04f6e-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="04f6e-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f6e-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="04f6e-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="04f6e-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f6e-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="04f6e-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="04f6e-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04f6e-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="04f6e-117">Class of the RR.</span></span> <span data-ttu-id="04f6e-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="04f6e-118">Default value is 1.</span></span> <span data-ttu-id="04f6e-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="04f6e-119">The following values are valid.</span></span>



| <span data-ttu-id="04f6e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="04f6e-120">Value</span></span>                                                                                                | <span data-ttu-id="04f6e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="04f6e-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="04f6e-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="04f6e-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="04f6e-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="04f6e-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="04f6e-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="04f6e-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="04f6e-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="04f6e-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="04f6e-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="04f6e-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="04f6e-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="04f6e-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="04f6e-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="04f6e-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="04f6e-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="04f6e-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="04f6e-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04f6e-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="04f6e-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="04f6e-132">*Респонсиблемаилбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-132">*ResponsibleMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f6e-133">Полное доменное имя, указывающее почтовый ящик, отвечающий за список рассылки или почтовый ящик, указанный в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="04f6e-133">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="04f6e-134">*Еррормаилбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-134">*ErrorMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f6e-135">Полное доменное имя, указывающее почтовый ящик для получения сообщений об ошибках, относящихся к списку рассылки, или к почтовому ящику, указанному именем владельца записи MINFO.</span><span class="sxs-lookup"><span data-stu-id="04f6e-135">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="04f6e-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="04f6e-137">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="04f6e-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f6e-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04f6e-138">Return value</span></span>

<span data-ttu-id="04f6e-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="04f6e-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f6e-140">Требования</span><span class="sxs-lookup"><span data-stu-id="04f6e-140">Requirements</span></span>



| <span data-ttu-id="04f6e-141">Требование</span><span class="sxs-lookup"><span data-stu-id="04f6e-141">Requirement</span></span> | <span data-ttu-id="04f6e-142">Значение</span><span class="sxs-lookup"><span data-stu-id="04f6e-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04f6e-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04f6e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="04f6e-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="04f6e-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="04f6e-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04f6e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="04f6e-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04f6e-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="04f6e-147">Namespace</span></span><br/>                | <span data-ttu-id="04f6e-148">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="04f6e-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="04f6e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="04f6e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04f6e-150"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04f6e-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f6e-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04f6e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f6e-152">**Микрософтднс \_ минфотипе**</span><span class="sxs-lookup"><span data-stu-id="04f6e-152">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="04f6e-153">**Метод Modify \_ класса микрософтднс минфотипе**</span><span class="sxs-lookup"><span data-stu-id="04f6e-153">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="04f6e-154">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="04f6e-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





