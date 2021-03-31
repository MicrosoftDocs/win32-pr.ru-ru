---
title: Метод Modify класса MicrosoftDNS_AType
description: Метод Modify обновляет TTL и IP-адрес записи ресурса адреса узла (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_AType класс
- MicrosoftDNS_AType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071635"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="99d72-106">Метод Modify \_ класса микрософтднс атипе</span><span class="sxs-lookup"><span data-stu-id="99d72-106">Modify method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="99d72-107">Метод **Modify** обновляет TTL и IP-адрес записи ресурса адреса узла (a).</span><span class="sxs-lookup"><span data-stu-id="99d72-107">The **Modify** method updates the TTL and IP address of a host Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="99d72-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99d72-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="99d72-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="99d72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99d72-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="99d72-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="99d72-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="99d72-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="99d72-112">*IP-адрес* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="99d72-112">*IPAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="99d72-113">Строка, представляющая IP-адрес узла.</span><span class="sxs-lookup"><span data-stu-id="99d72-113">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="99d72-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="99d72-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="99d72-115">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="99d72-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99d72-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99d72-116">Return value</span></span>

<span data-ttu-id="99d72-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="99d72-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99d72-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99d72-118">Remarks</span></span>

<span data-ttu-id="99d72-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="99d72-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="99d72-120">Требования</span><span class="sxs-lookup"><span data-stu-id="99d72-120">Requirements</span></span>



| <span data-ttu-id="99d72-121">Требование</span><span class="sxs-lookup"><span data-stu-id="99d72-121">Requirement</span></span> | <span data-ttu-id="99d72-122">Значение</span><span class="sxs-lookup"><span data-stu-id="99d72-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99d72-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99d72-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99d72-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="99d72-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="99d72-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99d72-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99d72-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99d72-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99d72-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="99d72-127">Namespace</span></span><br/>                | <span data-ttu-id="99d72-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="99d72-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="99d72-129">MOF</span><span class="sxs-lookup"><span data-stu-id="99d72-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99d72-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99d72-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99d72-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99d72-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99d72-132">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="99d72-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="99d72-133">**Метод Креатеинстанцефромпропертидата \_ класса Атипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="99d72-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





