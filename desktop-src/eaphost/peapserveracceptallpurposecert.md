---
title: пеапсерверакцепталлпурпосецерт
description: Раздел реестра Пеапсерверакцепталлпурпосецерт определяет, принимаются ли сертификаты всех целей для проверки подлинности PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105691424"
---
# <a name="peapserveracceptallpurposecert"></a><span data-ttu-id="38ce3-103">пеапсерверакцепталлпурпосецерт</span><span class="sxs-lookup"><span data-stu-id="38ce3-103">PeapServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="38ce3-104">Раздел реестра Пеапсерверакцепталлпурпосецерт определяет, принимаются ли сертификаты всех целей для проверки подлинности PEAP.</span><span class="sxs-lookup"><span data-stu-id="38ce3-104">The PeapServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="38ce3-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="38ce3-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="38ce3-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38ce3-106">Remarks</span></span>

<span data-ttu-id="38ce3-107">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="38ce3-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="38ce3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="38ce3-108">Value</span></span>        | <span data-ttu-id="38ce3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="38ce3-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ce3-110">1</span><span class="sxs-lookup"><span data-stu-id="38ce3-110">1</span></span>            | <span data-ttu-id="38ce3-111">Сервер и клиент принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="38ce3-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="38ce3-112">Другие значения</span><span class="sxs-lookup"><span data-stu-id="38ce3-112">Other values</span></span> | <span data-ttu-id="38ce3-113">Сервер и клиент не принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="38ce3-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="38ce3-114">Если этот параметр реестра отсутствует, сервер и клиент принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности PEAP.</span><span class="sxs-lookup"><span data-stu-id="38ce3-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38ce3-115">См. также</span><span class="sxs-lookup"><span data-stu-id="38ce3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38ce3-116">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="38ce3-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




