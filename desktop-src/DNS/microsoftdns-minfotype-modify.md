---
title: Метод Modify класса MicrosoftDNS_MINFOType
description: Метод Modify обновляет запись ресурса почтовых сообщений (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MINFOType класс
- MicrosoftDNS_MINFOType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489774"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="0e728-106">Метод Modify \_ класса микрософтднс минфотипе</span><span class="sxs-lookup"><span data-stu-id="0e728-106">Modify method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="0e728-107">Метод **Modify** обновляет запись ресурса почтовых сообщений (MINFO).</span><span class="sxs-lookup"><span data-stu-id="0e728-107">The **Modify** method updates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e728-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e728-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="0e728-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e728-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e728-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0e728-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e728-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="0e728-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="0e728-112">*Респонсиблемаилбокс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0e728-112">*ResponsibleMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e728-113">Полное доменное имя, указывающее почтовый ящик, отвечающий за список рассылки или почтовый ящик, указанный в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="0e728-113">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="0e728-114">*Еррормаилбокс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0e728-114">*ErrorMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e728-115">Полное доменное имя, указывающее почтовый ящик для получения сообщений об ошибках, относящихся к списку рассылки, или к почтовому ящику, указанному именем владельца записи MINFO.</span><span class="sxs-lookup"><span data-stu-id="0e728-115">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="0e728-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="0e728-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0e728-117">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="0e728-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e728-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e728-118">Return value</span></span>

<span data-ttu-id="0e728-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0e728-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e728-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e728-120">Remarks</span></span>

<span data-ttu-id="0e728-121">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="0e728-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e728-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0e728-122">Requirements</span></span>



| <span data-ttu-id="0e728-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0e728-123">Requirement</span></span> | <span data-ttu-id="0e728-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0e728-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e728-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e728-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0e728-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0e728-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0e728-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e728-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0e728-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e728-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0e728-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0e728-129">Namespace</span></span><br/>                | <span data-ttu-id="0e728-130">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="0e728-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="0e728-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0e728-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e728-132"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e728-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e728-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e728-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e728-134">**Микрософтднс \_ минфотипе**</span><span class="sxs-lookup"><span data-stu-id="0e728-134">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="0e728-135">**Метод Креатеинстанцефромпропертидата \_ класса Минфотипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="0e728-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="0e728-136">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="0e728-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





