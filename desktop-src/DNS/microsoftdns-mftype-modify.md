---
title: Метод Modify класса MicrosoftDNS_MFType
description: Метод Modify обновляет запись ресурса агента переадресации почты для домена (MF).
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MFType класс
- MicrosoftDNS_MFType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0a363290580c7cecf47dbe00c6dd7895d23dbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491733"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="b8ff1-106">Метод Modify \_ класса микрософтднс мфтипе</span><span class="sxs-lookup"><span data-stu-id="b8ff1-106">Modify method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="b8ff1-107">Метод **Modify** обновляет запись ресурса агента переадресации почты для домена (MF).</span><span class="sxs-lookup"><span data-stu-id="b8ff1-107">The **Modify** method updates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ff1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8ff1-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b8ff1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8ff1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ff1-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b8ff1-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ff1-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b8ff1-112">*Мфхост* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b8ff1-112">*MFHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ff1-113">Имя узла, предоставляющего агент пересылки почты.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-113">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="b8ff1-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="b8ff1-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ff1-115">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8ff1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8ff1-116">Return value</span></span>

<span data-ttu-id="b8ff1-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ff1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8ff1-118">Remarks</span></span>

<span data-ttu-id="b8ff1-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ff1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b8ff1-120">Requirements</span></span>



| <span data-ttu-id="b8ff1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b8ff1-121">Requirement</span></span> | <span data-ttu-id="b8ff1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b8ff1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ff1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8ff1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ff1-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b8ff1-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b8ff1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8ff1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ff1-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8ff1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b8ff1-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b8ff1-127">Namespace</span></span><br/>                | <span data-ttu-id="b8ff1-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="b8ff1-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b8ff1-129">MOF</span><span class="sxs-lookup"><span data-stu-id="b8ff1-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8ff1-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8ff1-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ff1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8ff1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ff1-132">**Микрософтднс \_ мфтипе**</span><span class="sxs-lookup"><span data-stu-id="b8ff1-132">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="b8ff1-133">**Метод Креатеинстанцефромпропертидата \_ класса Мфтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="b8ff1-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b8ff1-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="b8ff1-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





