---
title: Метод Modify класса MicrosoftDNS_WKSType
description: Метод Modify обновляет запись ресурса Well-Known Services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_WKSType класс
- MicrosoftDNS_WKSType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892213"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="2bcfb-106">Метод Modify \_ класса микрософтднс вкстипе</span><span class="sxs-lookup"><span data-stu-id="2bcfb-106">Modify method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="2bcfb-107">Метод **Modify** обновляет запись ресурса Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="2bcfb-107">The **Modify** method updates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bcfb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bcfb-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2bcfb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bcfb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bcfb-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2bcfb-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcfb-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfb-112">*Интернетаддресс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2bcfb-112">*InternetAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcfb-113">IP-адрес владельца записи.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-113">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfb-114">*Иппротокол* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2bcfb-114">*IPProtocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcfb-115">Строка, представляющая протокол IP для этой записи.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-115">String representing the IP protocol for this record.</span></span> <span data-ttu-id="2bcfb-116">Допустимые значения: UDP или TCP.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-116">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfb-117">*Службы* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2bcfb-117">*Services* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcfb-118">Строка, содержащая все службы, используемые записью службы хорошо известных служб (WKS).</span><span class="sxs-lookup"><span data-stu-id="2bcfb-118">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfb-119">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="2bcfb-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcfb-120">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bcfb-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bcfb-121">Return value</span></span>

<span data-ttu-id="2bcfb-122">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bcfb-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bcfb-123">Remarks</span></span>

<span data-ttu-id="2bcfb-124">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bcfb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2bcfb-125">Requirements</span></span>



| <span data-ttu-id="2bcfb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2bcfb-126">Requirement</span></span> | <span data-ttu-id="2bcfb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2bcfb-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcfb-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bcfb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2bcfb-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2bcfb-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2bcfb-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bcfb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2bcfb-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2bcfb-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2bcfb-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2bcfb-132">Namespace</span></span><br/>                | <span data-ttu-id="2bcfb-133">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="2bcfb-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2bcfb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2bcfb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bcfb-135"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bcfb-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bcfb-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bcfb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcfb-137">**Микрософтднс \_ вкстипе**</span><span class="sxs-lookup"><span data-stu-id="2bcfb-137">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="2bcfb-138">**Метод Креатеинстанцефромпропертидата \_ класса Вкстипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="2bcfb-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2bcfb-139">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="2bcfb-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





