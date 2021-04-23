---
title: тлссерверусеаллпурпосецерт
description: Раздел реестра Тлссерверусеаллпурпосецерт определяет, используются ли для проверки подлинности EAP-TLS сертификаты всех целей.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104335712"
---
# <a name="tlsserveruseallpurposecert"></a><span data-ttu-id="ab92c-103">тлссерверусеаллпурпосецерт</span><span class="sxs-lookup"><span data-stu-id="ab92c-103">TlsServerUseAllPurposeCert</span></span>

<span data-ttu-id="ab92c-104">Раздел реестра Тлссерверусеаллпурпосецерт определяет, используются ли для проверки подлинности EAP-TLS сертификаты всех целей.</span><span class="sxs-lookup"><span data-stu-id="ab92c-104">The TlsServerUseAllPurposeCert registry key determines if all-purpose certificates are used for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ab92c-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="ab92c-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="ab92c-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab92c-106">Remarks</span></span>

<span data-ttu-id="ab92c-107">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ab92c-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="ab92c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ab92c-108">Value</span></span>        | <span data-ttu-id="ab92c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ab92c-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab92c-110">1</span><span class="sxs-lookup"><span data-stu-id="ab92c-110">1</span></span>            | <span data-ttu-id="ab92c-111">Для проверки подлинности PEAP выбираются сертификаты всех целей в хранилище сертификатов клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="ab92c-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="ab92c-112">Другие значения</span><span class="sxs-lookup"><span data-stu-id="ab92c-112">Other values</span></span> | <span data-ttu-id="ab92c-113">Сертификаты всех целей в хранилище сертификатов клиента или сервера не выбраны для проверки подлинности PEAP.</span><span class="sxs-lookup"><span data-stu-id="ab92c-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="ab92c-114">Если это значение реестра отсутствует, для проверки подлинности EAP-TLS выбираются сертификаты всех целей в хранилище сертификатов клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="ab92c-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab92c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ab92c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab92c-116">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="ab92c-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




