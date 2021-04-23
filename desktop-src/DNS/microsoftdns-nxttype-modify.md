---
title: Метод Modify класса MicrosoftDNS_NXTType
description: Метод Modify обновляет следующую запись ресурса (NXT).
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_NXTType класс
- MicrosoftDNS_NXTType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489771"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="b841a-106">Метод Modify \_ класса микрософтднс нксттипе</span><span class="sxs-lookup"><span data-stu-id="b841a-106">Modify method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="b841a-107">Метод **Modify** обновляет следующую запись ресурса (NXT).</span><span class="sxs-lookup"><span data-stu-id="b841a-107">The **Modify** method updates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b841a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b841a-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b841a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b841a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b841a-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b841a-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b841a-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="b841a-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b841a-112">*Некстдомаиннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b841a-112">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b841a-113">Следующее имя домена.</span><span class="sxs-lookup"><span data-stu-id="b841a-113">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b841a-114">*Типы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b841a-114">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b841a-115">Разделенный пробелами список назначенных пространств имен для имени владельца записи ресурса NXT.</span><span class="sxs-lookup"><span data-stu-id="b841a-115">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="b841a-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="b841a-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b841a-117">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="b841a-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b841a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b841a-118">Return value</span></span>

<span data-ttu-id="b841a-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b841a-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b841a-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b841a-120">Remarks</span></span>

<span data-ttu-id="b841a-121">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="b841a-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="b841a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b841a-122">Requirements</span></span>



| <span data-ttu-id="b841a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b841a-123">Requirement</span></span> | <span data-ttu-id="b841a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b841a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b841a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b841a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b841a-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b841a-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b841a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b841a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b841a-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b841a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b841a-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b841a-129">Namespace</span></span><br/>                | <span data-ttu-id="b841a-130">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="b841a-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b841a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b841a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b841a-132"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b841a-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b841a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b841a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b841a-134">**Микрософтднс \_ нксттипе**</span><span class="sxs-lookup"><span data-stu-id="b841a-134">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="b841a-135">**Метод Креатеинстанцефромпропертидата \_ класса Нксттипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="b841a-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b841a-136">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="b841a-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





