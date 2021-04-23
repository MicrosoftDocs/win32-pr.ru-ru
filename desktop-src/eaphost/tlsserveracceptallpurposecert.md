---
title: тлссерверакцепталлпурпосецерт
description: Раздел реестра Тлссерверакцепталлпурпосецерт определяет, принимаются ли сертификаты всех целей для проверки подлинности EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105661675"
---
# <a name="tlsserveracceptallpurposecert"></a><span data-ttu-id="f02cd-103">тлссерверакцепталлпурпосецерт</span><span class="sxs-lookup"><span data-stu-id="f02cd-103">TlsServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="f02cd-104">Раздел реестра Тлссерверакцепталлпурпосецерт определяет, принимаются ли сертификаты всех целей для проверки подлинности EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="f02cd-104">The TlsServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f02cd-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="f02cd-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="f02cd-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f02cd-106">Remarks</span></span>

<span data-ttu-id="f02cd-107">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f02cd-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="f02cd-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f02cd-108">Value</span></span>        | <span data-ttu-id="f02cd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f02cd-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02cd-110">1</span><span class="sxs-lookup"><span data-stu-id="f02cd-110">1</span></span>            | <span data-ttu-id="f02cd-111">Сервер и клиент принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="f02cd-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="f02cd-112">Другие значения</span><span class="sxs-lookup"><span data-stu-id="f02cd-112">Other values</span></span> | <span data-ttu-id="f02cd-113">Сервер и клиент не принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="f02cd-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="f02cd-114">Если это значение реестра отсутствует, сервер и клиент принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="f02cd-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f02cd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f02cd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f02cd-116">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="f02cd-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




