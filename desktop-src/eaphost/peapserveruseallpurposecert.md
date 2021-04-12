---
title: пеапсерверусеаллпурпосецерт
description: Раздел реестра Пеапсерверусеаллпурпосецерт определяет, используются ли для проверки подлинности PEAP сертификаты всех целей.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104335739"
---
# <a name="peapserveruseallpurposecert"></a><span data-ttu-id="e9b9e-103">пеапсерверусеаллпурпосецерт</span><span class="sxs-lookup"><span data-stu-id="e9b9e-103">PeapServerUseAllPurposeCert</span></span>

<span data-ttu-id="e9b9e-104">Раздел реестра Пеапсерверусеаллпурпосецерт определяет, используются ли для проверки подлинности PEAP сертификаты всех целей.</span><span class="sxs-lookup"><span data-stu-id="e9b9e-104">The PeapServerUseAllPurposeCert registry key determines if all-purpose certificates are used for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e9b9e-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="e9b9e-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="e9b9e-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9b9e-106">Remarks</span></span>

<span data-ttu-id="e9b9e-107">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e9b9e-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="e9b9e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e9b9e-108">Value</span></span>        | <span data-ttu-id="e9b9e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e9b9e-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b9e-110">1</span><span class="sxs-lookup"><span data-stu-id="e9b9e-110">1</span></span>            | <span data-ttu-id="e9b9e-111">Для проверки подлинности PEAP выбираются сертификаты всех целей в хранилище сертификатов клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="e9b9e-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="e9b9e-112">Другие значения</span><span class="sxs-lookup"><span data-stu-id="e9b9e-112">Other values</span></span> | <span data-ttu-id="e9b9e-113">Сертификаты всех целей в хранилище сертификатов клиента или сервера не выбраны для проверки подлинности PEAP.</span><span class="sxs-lookup"><span data-stu-id="e9b9e-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="e9b9e-114">Если это значение реестра отсутствует, для аутентификации PEAP выбираются сертификаты всех целей в хранилище сертификатов клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="e9b9e-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9b9e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e9b9e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9b9e-116">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="e9b9e-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




