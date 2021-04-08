---
title: Метод Стартскавенгинг класса MicrosoftDNS_Server
description: Метод Стартскавенгинг запускает очистку устаревших записей в зонах, подлежащим очистке.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- DNS-метод Стартскавенгинг
- Стартскавенгинг метода DNS, класс MicrosoftDNS_Server
- DNS класса MicrosoftDNS_Server, метод Стартскавенгинг
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988805"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="df553-106">Метод Стартскавенгинг \_ класса микрософтднс Server</span><span class="sxs-lookup"><span data-stu-id="df553-106">StartScavenging method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="df553-107">Метод **стартскавенгинг** запускает очистку устаревших записей в зонах, подлежащим очистке.</span><span class="sxs-lookup"><span data-stu-id="df553-107">The **StartScavenging** method starts scavenging stale records in the zones subjected to scavenging.</span></span>

## <a name="syntax"></a><span data-ttu-id="df553-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df553-108">Syntax</span></span>


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a><span data-ttu-id="df553-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="df553-109">Parameters</span></span>

<span data-ttu-id="df553-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="df553-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df553-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df553-111">Return value</span></span>

<span data-ttu-id="df553-112">Ошибка \_ указывает, что очистка успешно запущена.</span><span class="sxs-lookup"><span data-stu-id="df553-112">ERROR\_SUCCESS indicates the scavenging was successfully started.</span></span> <span data-ttu-id="df553-113">Любое другое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="df553-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="df553-114">Требования</span><span class="sxs-lookup"><span data-stu-id="df553-114">Requirements</span></span>



| <span data-ttu-id="df553-115">Требование</span><span class="sxs-lookup"><span data-stu-id="df553-115">Requirement</span></span> | <span data-ttu-id="df553-116">Значение</span><span class="sxs-lookup"><span data-stu-id="df553-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df553-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df553-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df553-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="df553-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="df553-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df553-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df553-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df553-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="df553-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="df553-121">Namespace</span></span><br/>                | <span data-ttu-id="df553-122">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="df553-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="df553-123">MOF</span><span class="sxs-lookup"><span data-stu-id="df553-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df553-124"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df553-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df553-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df553-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df553-126">**\_Сервер микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="df553-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="df553-127">**Метод StartService \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="df553-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="df553-128">**Метод работы \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="df553-128">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="df553-129">**Метод Жетдистингуишеднаме \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="df553-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





