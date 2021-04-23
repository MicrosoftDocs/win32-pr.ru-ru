---
title: Метод Креатеинстанцефромтекстрепресентатион класса MicrosoftDNS_ResourceRecord
description: Метод Креатеинстанцефромтекстрепресентатион создает экземпляр \_ объекта микрософтднс ресаурцерекорд.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- DNS-метод Креатеинстанцефромтекстрепресентатион
- Креатеинстанцефромтекстрепресентатион метода DNS, класс MicrosoftDNS_ResourceRecord
- DNS класса MicrosoftDNS_ResourceRecord, метод Креатеинстанцефромтекстрепресентатион
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071733"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="9bea3-106">Метод Креатеинстанцефромтекстрепресентатион \_ класса Ресаурцерекорд микрософтднс</span><span class="sxs-lookup"><span data-stu-id="9bea3-106">CreateInstanceFromTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="9bea3-107">Метод **креатеинстанцефромтекстрепресентатион** создает экземпляр объекта [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="9bea3-107">The **CreateInstanceFromTextRepresentation** method instantiates a [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bea3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bea3-108">Syntax</span></span>


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9bea3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bea3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bea3-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bea3-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bea3-111">Имя DNS-сервера, на котором должна быть создана запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="9bea3-111">Name of the DNS Server on which the RR should be created.</span></span>

</dd> <dt>

<span data-ttu-id="9bea3-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bea3-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bea3-113">Имя контейнера, в который следует поместить новую запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="9bea3-113">Name of the container into which the new RR should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="9bea3-114">*Текстрепресентатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bea3-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bea3-115">Текстовое представление создаваемого экземпляра RR.</span><span class="sxs-lookup"><span data-stu-id="9bea3-115">Text representation of the RR instance to be created.</span></span>

</dd> <dt>

<span data-ttu-id="9bea3-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="9bea3-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9bea3-117">Ссылка на созданную запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="9bea3-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bea3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bea3-118">Return value</span></span>

<span data-ttu-id="9bea3-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9bea3-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bea3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9bea3-120">Requirements</span></span>



| <span data-ttu-id="9bea3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9bea3-121">Requirement</span></span> | <span data-ttu-id="9bea3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9bea3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bea3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bea3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9bea3-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9bea3-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9bea3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bea3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9bea3-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bea3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9bea3-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9bea3-127">Namespace</span></span><br/>                | <span data-ttu-id="9bea3-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="9bea3-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9bea3-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9bea3-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bea3-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bea3-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bea3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bea3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bea3-132">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="9bea3-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="9bea3-133">**Метод Жетобжектбитекстрепресентатион \_ класса Ресаурцерекорд микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9bea3-133">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





