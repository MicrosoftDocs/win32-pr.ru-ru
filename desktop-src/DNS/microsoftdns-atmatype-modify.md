---
title: Метод Modify класса MicrosoftDNS_ATMAType
description: Метод Modify обновляет запись ресурса ATM Address to Name (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_ATMAType класс
- MicrosoftDNS_ATMAType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071636"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="cc25f-106">Метод Modify \_ класса микрософтднс атматипе</span><span class="sxs-lookup"><span data-stu-id="cc25f-106">Modify method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="cc25f-107">Метод **Modify** обновляет запись ресурса ATM Address to Name (ATMA).</span><span class="sxs-lookup"><span data-stu-id="cc25f-107">The **Modify** method updates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc25f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc25f-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="cc25f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc25f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc25f-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cc25f-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc25f-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="cc25f-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="cc25f-112">*Формат* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cc25f-112">*Format* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc25f-113">Формат адреса ATM.</span><span class="sxs-lookup"><span data-stu-id="cc25f-113">ATM address format.</span></span> <span data-ttu-id="cc25f-114">ФОРМАТ имеет два возможных значения: 0, указывающий формат адреса конечной системы (АЕСА) ATM, а 1 — формат E. 164.</span><span class="sxs-lookup"><span data-stu-id="cc25f-114">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="cc25f-115">*Атмаддресс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cc25f-115">*ATMAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc25f-116">Строка переменной длины октетов, содержащая ATM-адрес узла или владельца, к которому относится эта запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc25f-116">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="cc25f-117">Первые четыре байта массива используются для хранения размера строки октета.</span><span class="sxs-lookup"><span data-stu-id="cc25f-117">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="cc25f-118">Наиболее значимый байт хранится в байте 0.</span><span class="sxs-lookup"><span data-stu-id="cc25f-118">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="cc25f-119">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="cc25f-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cc25f-120">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="cc25f-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc25f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc25f-121">Return value</span></span>

<span data-ttu-id="cc25f-122">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cc25f-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc25f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc25f-123">Remarks</span></span>

<span data-ttu-id="cc25f-124">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="cc25f-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc25f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="cc25f-125">Requirements</span></span>



| <span data-ttu-id="cc25f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="cc25f-126">Requirement</span></span> | <span data-ttu-id="cc25f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cc25f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc25f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc25f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cc25f-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc25f-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cc25f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc25f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cc25f-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc25f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc25f-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cc25f-132">Namespace</span></span><br/>                | <span data-ttu-id="cc25f-133">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="cc25f-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cc25f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cc25f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc25f-135"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc25f-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc25f-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc25f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc25f-137">**Микрософтднс \_ атматипе**</span><span class="sxs-lookup"><span data-stu-id="cc25f-137">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="cc25f-138">**Метод Креатеинстанцефромпропертидата \_ класса Атматипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc25f-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="cc25f-139">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="cc25f-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





