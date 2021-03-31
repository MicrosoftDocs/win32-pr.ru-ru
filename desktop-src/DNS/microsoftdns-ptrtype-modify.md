---
title: Метод Modify класса MicrosoftDNS_PTRType
description: Метод Modify обновляет запись ресурса указателя (PTR).
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_PTRType класс
- MicrosoftDNS_PTRType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988810"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="3a254-106">Метод Modify \_ класса микрософтднс птртипе</span><span class="sxs-lookup"><span data-stu-id="3a254-106">Modify method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="3a254-107">Метод **Modify** обновляет запись ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="3a254-107">The **Modify** method updates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a254-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a254-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3a254-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a254-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a254-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3a254-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a254-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="3a254-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3a254-112">*Птрдомаиннаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3a254-112">*PTRDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a254-113">Адрес имени домена записи PTR.</span><span class="sxs-lookup"><span data-stu-id="3a254-113">Domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="3a254-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="3a254-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3a254-115">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="3a254-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a254-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a254-116">Return value</span></span>

<span data-ttu-id="3a254-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3a254-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a254-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a254-118">Remarks</span></span>

<span data-ttu-id="3a254-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="3a254-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a254-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3a254-120">Requirements</span></span>



| <span data-ttu-id="3a254-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3a254-121">Requirement</span></span> | <span data-ttu-id="3a254-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3a254-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a254-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a254-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3a254-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a254-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3a254-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a254-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3a254-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3a254-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3a254-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a254-127">Namespace</span></span><br/>                | <span data-ttu-id="3a254-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="3a254-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3a254-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3a254-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a254-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a254-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a254-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a254-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a254-132">**Микрософтднс \_ птртипе**</span><span class="sxs-lookup"><span data-stu-id="3a254-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="3a254-133">**Метод Креатеинстанцефромпропертидата \_ класса Птртипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="3a254-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3a254-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="3a254-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





