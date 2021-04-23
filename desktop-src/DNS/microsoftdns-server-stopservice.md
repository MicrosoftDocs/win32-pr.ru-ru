---
title: Метод «начало» класса MicrosoftDNS_Server
description: Метод «незавершенный» останавливает работу DNS-сервера.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- DNS-метод "без"
- Метод "в DNS", MicrosoftDNS_Server класс
- DNS класса MicrosoftDNS_Server, метод "некоторая"
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491160"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="dd9c3-106">Метод работы \_ класса микрософтднс Server</span><span class="sxs-lookup"><span data-stu-id="dd9c3-106">StopService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="dd9c3-107">Метод **«** незавершенный» останавливает работу DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="dd9c3-107">The **StopService** method stops the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd9c3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd9c3-108">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="dd9c3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd9c3-109">Parameters</span></span>

<span data-ttu-id="dd9c3-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dd9c3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd9c3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd9c3-111">Return value</span></span>

<span data-ttu-id="dd9c3-112">Ошибка \_ указывает на успешную остановку службы.</span><span class="sxs-lookup"><span data-stu-id="dd9c3-112">ERROR\_SUCCESS indicates the service was successfully stopped.</span></span> <span data-ttu-id="dd9c3-113">Любое другое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="dd9c3-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd9c3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="dd9c3-114">Requirements</span></span>



| <span data-ttu-id="dd9c3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="dd9c3-115">Requirement</span></span> | <span data-ttu-id="dd9c3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dd9c3-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd9c3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd9c3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dd9c3-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd9c3-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dd9c3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd9c3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dd9c3-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd9c3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dd9c3-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd9c3-121">Namespace</span></span><br/>                | <span data-ttu-id="dd9c3-122">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="dd9c3-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dd9c3-123">MOF</span><span class="sxs-lookup"><span data-stu-id="dd9c3-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd9c3-124"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd9c3-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd9c3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd9c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd9c3-126">**\_Сервер микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="dd9c3-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="dd9c3-127">**Метод StartService \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="dd9c3-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="dd9c3-128">**Метод Стартскавенгинг \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="dd9c3-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="dd9c3-129">**Метод Жетдистингуишеднаме \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="dd9c3-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





