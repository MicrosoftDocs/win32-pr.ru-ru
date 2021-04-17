---
title: Метод Жетобжектбитекстрепресентатион класса MicrosoftDNS_ResourceRecord
description: Метод Жетобжектбитекстрепресентатион извлекает существующий экземпляр \_ класса Ресаурцерекорд микрософтднс.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- DNS-метод Жетобжектбитекстрепресентатион
- Жетобжектбитекстрепресентатион метода DNS, класс MicrosoftDNS_ResourceRecord
- DNS класса MicrosoftDNS_ResourceRecord, метод Жетобжектбитекстрепресентатион
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491169"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="11896-106">Метод Жетобжектбитекстрепресентатион \_ класса Ресаурцерекорд микрософтднс</span><span class="sxs-lookup"><span data-stu-id="11896-106">GetObjectByTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="11896-107">Метод **жетобжектбитекстрепресентатион** извлекает существующий экземпляр класса [**\_ ресаурцерекорд микрософтднс**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="11896-107">The **GetObjectByTextRepresentation** method retrieves an existing instance of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="11896-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11896-108">Syntax</span></span>


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a><span data-ttu-id="11896-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="11896-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11896-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11896-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11896-111">Имя DNS-сервера, с которого должна быть получена запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="11896-111">Name of the DNS Server from which the RR should be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="11896-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11896-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11896-113">Имя контейнера, из которого должна быть получена запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="11896-113">Name of the container from which the RR should be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="11896-114">*Текстрепресентатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11896-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11896-115">Текстовое представление извлекаемой записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="11896-115">Text representation of the RR to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="11896-116">*RR* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11896-116">*RR* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11896-117">Ссылка на созданную запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="11896-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11896-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11896-118">Return value</span></span>

<span data-ttu-id="11896-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="11896-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="11896-120">Требования</span><span class="sxs-lookup"><span data-stu-id="11896-120">Requirements</span></span>



| <span data-ttu-id="11896-121">Требование</span><span class="sxs-lookup"><span data-stu-id="11896-121">Requirement</span></span> | <span data-ttu-id="11896-122">Значение</span><span class="sxs-lookup"><span data-stu-id="11896-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11896-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11896-123">Minimum supported client</span></span><br/> | <span data-ttu-id="11896-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="11896-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="11896-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11896-125">Minimum supported server</span></span><br/> | <span data-ttu-id="11896-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11896-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="11896-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11896-127">Namespace</span></span><br/>                | <span data-ttu-id="11896-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="11896-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="11896-129">MOF</span><span class="sxs-lookup"><span data-stu-id="11896-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11896-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11896-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11896-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11896-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11896-132">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="11896-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="11896-133">**Метод Креатеинстанцефромтекстрепресентатион \_ класса Ресаурцерекорд микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="11896-133">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





