---
title: Метод Modify класса MicrosoftDNS_AFSDBType
description: Метод Modify обновляет запись ресурса сервера базы данных файловой системы AFS (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_AFSDBType класс
- MicrosoftDNS_AFSDBType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654494"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="c4b0d-106">Метод Modify \_ класса микрософтднс афсдбтипе</span><span class="sxs-lookup"><span data-stu-id="c4b0d-106">Modify method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="c4b0d-107">Метод **Modify** обновляет запись ресурса сервера базы данных файловой системы AFS (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="c4b0d-107">The **Modify** method updates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b0d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4b0d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c4b0d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4b0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4b0d-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c4b0d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b0d-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c4b0d-112">*Подтип* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c4b0d-112">*Subtype* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b0d-113">Подтип ведущего сервера AFS.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-113">Subtype of the host AFS server.</span></span> <span data-ttu-id="c4b0d-114">Для подтипа 1 (значение 1) на узле имеется сервер AFS версии 3,0 для именованной ячейки AFS.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-114">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="c4b0d-115">В случае подтипа 2 (значение = 2) узел имеет прошедший проверку подлинности сервер имен, в котором размещен узел корневого каталога ячеек для именованной ячейки DCE/NCA.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-115">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="c4b0d-116">*Имя сервера* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c4b0d-116">*ServerName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b0d-117">Полное доменное имя, указывающее узел с сервером для ячейки AFS, указанной в имени владельца.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-117">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="c4b0d-118">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="c4b0d-118">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b0d-119">Ссылка на измененный объект.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-119">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4b0d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4b0d-120">Return value</span></span>

<span data-ttu-id="c4b0d-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4b0d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4b0d-122">Remarks</span></span>

<span data-ttu-id="c4b0d-123">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-123">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4b0d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c4b0d-124">Requirements</span></span>



| <span data-ttu-id="c4b0d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c4b0d-125">Requirement</span></span> | <span data-ttu-id="c4b0d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c4b0d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b0d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4b0d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c4b0d-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c4b0d-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c4b0d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4b0d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c4b0d-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4b0d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4b0d-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4b0d-131">Namespace</span></span><br/>                | <span data-ttu-id="c4b0d-132">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="c4b0d-132">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c4b0d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c4b0d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4b0d-134"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4b0d-134"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4b0d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4b0d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4b0d-136">**Микрософтднс \_ афсдбтипе**</span><span class="sxs-lookup"><span data-stu-id="c4b0d-136">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="c4b0d-137">**Метод Креатеинстанцефромпропертидата \_ класса Афсдбтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="c4b0d-137">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c4b0d-138">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="c4b0d-138">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





