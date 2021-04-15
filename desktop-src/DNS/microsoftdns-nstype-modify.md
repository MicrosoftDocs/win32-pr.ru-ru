---
title: Метод Modify класса MicrosoftDNS_NSType
description: Метод Modify обновляет запись ресурса сервера имен (NS).
ms.assetid: da625231-cf4e-4526-b713-737e6b9f5831
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_NSType класс
- MicrosoftDNS_NSType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3dd26b7c0f1c31ef3ea742f20f70df8646a087b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493293"
---
# <a name="modify-method-of-the-microsoftdns_nstype-class"></a><span data-ttu-id="b957e-106">Метод Modify \_ класса микрософтднс нстипе</span><span class="sxs-lookup"><span data-stu-id="b957e-106">Modify method of the MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="b957e-107">Метод **Modify** обновляет запись ресурса сервера имен (NS).</span><span class="sxs-lookup"><span data-stu-id="b957e-107">The **Modify** method updates a Name Server (NS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b957e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b957e-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b957e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b957e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b957e-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b957e-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b957e-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="b957e-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b957e-112">*Ншост* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b957e-112">*NSHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b957e-113">Полномочный узел для домена.</span><span class="sxs-lookup"><span data-stu-id="b957e-113">Authoritative host for the domain.</span></span>

</dd> <dt>

<span data-ttu-id="b957e-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="b957e-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b957e-115">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="b957e-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b957e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b957e-116">Return value</span></span>

<span data-ttu-id="b957e-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b957e-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b957e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b957e-118">Remarks</span></span>

<span data-ttu-id="b957e-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="b957e-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="b957e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b957e-120">Requirements</span></span>



| <span data-ttu-id="b957e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b957e-121">Requirement</span></span> | <span data-ttu-id="b957e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b957e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b957e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b957e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b957e-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b957e-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b957e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b957e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b957e-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b957e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b957e-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b957e-127">Namespace</span></span><br/>                | <span data-ttu-id="b957e-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="b957e-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b957e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="b957e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b957e-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b957e-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b957e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b957e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b957e-132">**Микрософтднс \_ птртипе**</span><span class="sxs-lookup"><span data-stu-id="b957e-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="b957e-133">**Метод Креатеинстанцефромпропертидата \_ класса Птртипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="b957e-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b957e-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="b957e-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





