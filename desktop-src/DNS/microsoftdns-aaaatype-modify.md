---
title: Метод Modify класса MicrosoftDNS_AAAAType
description: Метод Modify обновляет запись ресурса IPv6-адреса (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_AAAAType класс
- MicrosoftDNS_AAAAType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891949"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="9dd68-106">Метод Modify \_ класса микрософтднс аааатипе</span><span class="sxs-lookup"><span data-stu-id="9dd68-106">Modify method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="9dd68-107">Метод **Modify** обновляет запись ресурса IPv6-адреса (AAAA).</span><span class="sxs-lookup"><span data-stu-id="9dd68-107">The **Modify** method updates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd68-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dd68-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9dd68-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dd68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd68-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9dd68-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd68-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="9dd68-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9dd68-112">*IPv6Address* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9dd68-112">*IPv6Address* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd68-113">IPv6-адрес узла.</span><span class="sxs-lookup"><span data-stu-id="9dd68-113">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="9dd68-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="9dd68-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd68-115">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="9dd68-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd68-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9dd68-116">Return value</span></span>

<span data-ttu-id="9dd68-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9dd68-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd68-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9dd68-118">Remarks</span></span>

<span data-ttu-id="9dd68-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="9dd68-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd68-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9dd68-120">Requirements</span></span>



| <span data-ttu-id="9dd68-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9dd68-121">Requirement</span></span> | <span data-ttu-id="9dd68-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9dd68-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd68-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9dd68-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd68-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9dd68-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9dd68-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9dd68-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd68-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9dd68-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9dd68-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9dd68-127">Namespace</span></span><br/>                | <span data-ttu-id="9dd68-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="9dd68-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9dd68-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9dd68-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9dd68-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9dd68-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dd68-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9dd68-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd68-132">**Микрософтднс \_ аааатипе**</span><span class="sxs-lookup"><span data-stu-id="9dd68-132">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="9dd68-133">**Метод Креатеинстанцефромпропертидата \_ класса Аааатипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9dd68-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9dd68-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="9dd68-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





