---
title: Метод Modify класса MicrosoftDNS_MGType
description: Метод Modify обновляет запись ресурса почтовой группы (MG).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MGType класс
- MicrosoftDNS_MGType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136603"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="43406-106">Метод Modify \_ класса микрософтднс мгтипе</span><span class="sxs-lookup"><span data-stu-id="43406-106">Modify method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="43406-107">Метод **Modify** обновляет запись ресурса почтовой группы (MG).</span><span class="sxs-lookup"><span data-stu-id="43406-107">The **Modify** method updates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="43406-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43406-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="43406-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="43406-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43406-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="43406-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43406-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="43406-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="43406-112">*Мгмаилбокс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="43406-112">*MGMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43406-113">Полное доменное имя, указывающее почтовый ящик, который является членом почтовой группы, указанной в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="43406-113">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="43406-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="43406-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="43406-115">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="43406-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43406-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43406-116">Return value</span></span>

<span data-ttu-id="43406-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="43406-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43406-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43406-118">Remarks</span></span>

<span data-ttu-id="43406-119">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="43406-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="43406-120">Требования</span><span class="sxs-lookup"><span data-stu-id="43406-120">Requirements</span></span>



| <span data-ttu-id="43406-121">Требование</span><span class="sxs-lookup"><span data-stu-id="43406-121">Requirement</span></span> | <span data-ttu-id="43406-122">Значение</span><span class="sxs-lookup"><span data-stu-id="43406-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43406-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43406-123">Minimum supported client</span></span><br/> | <span data-ttu-id="43406-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="43406-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="43406-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43406-125">Minimum supported server</span></span><br/> | <span data-ttu-id="43406-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43406-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="43406-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43406-127">Namespace</span></span><br/>                | <span data-ttu-id="43406-128">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="43406-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="43406-129">MOF</span><span class="sxs-lookup"><span data-stu-id="43406-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43406-130"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43406-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43406-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43406-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43406-132">**Микрософтднс \_ мгтипе**</span><span class="sxs-lookup"><span data-stu-id="43406-132">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="43406-133">**Метод Креатеинстанцефромпропертидата \_ класса Мгтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="43406-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="43406-134">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="43406-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





