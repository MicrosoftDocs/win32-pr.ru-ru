---
title: Метод Modify класса MicrosoftDNS_X25Type
description: Метод Modify обновляет запись ресурса X. 25 (X25).
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_X25Type класс
- MicrosoftDNS_X25Type класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10db2fa770d3da8487a712e631c41fdd4256bf7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136386"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="2b9e2-106">Метод Modify \_ класса микрософтднс X25Type</span><span class="sxs-lookup"><span data-stu-id="2b9e2-106">Modify method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="2b9e2-107">Метод **Modify** обновляет запись ресурса X. 25 (X25).</span><span class="sxs-lookup"><span data-stu-id="2b9e2-107">The **Modify** method updates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b9e2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b9e2-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2b9e2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b9e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b9e2-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2b9e2-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2b9e2-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="2b9e2-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="2b9e2-112">*Псднаддресс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2b9e2-112">*PSDNAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2b9e2-113">Адрес PSDN владельца записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="2b9e2-113">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="2b9e2-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="2b9e2-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2b9e2-115">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="2b9e2-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b9e2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b9e2-116">Return value</span></span>

<span data-ttu-id="2b9e2-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2b9e2-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b9e2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b9e2-118">Remarks</span></span>

<span data-ttu-id="2b9e2-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="2b9e2-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b9e2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2b9e2-120">Requirements</span></span>



| <span data-ttu-id="2b9e2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2b9e2-121">Requirement</span></span> | <span data-ttu-id="2b9e2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9e2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b9e2-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b9e2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b9e2-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2b9e2-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2b9e2-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b9e2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b9e2-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b9e2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2b9e2-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b9e2-127">Namespace</span></span><br/>                | <span data-ttu-id="2b9e2-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="2b9e2-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2b9e2-129">MOF</span><span class="sxs-lookup"><span data-stu-id="2b9e2-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b9e2-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b9e2-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b9e2-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b9e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b9e2-132">**Микрософтднс \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="2b9e2-132">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="2b9e2-133">**Метод Креатеинстанцефромпропертидата \_ класса X25Type микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="2b9e2-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2b9e2-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="2b9e2-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





