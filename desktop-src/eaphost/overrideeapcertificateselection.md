---
title: оверридиапцертификатеселектион
description: Раздел реестра Оверридиапцертификатеселектион определяет, будет ли клиент переопределять поведение выбора сертификата смарт-карты по умолчанию и предоставлять пользователю больше сертификатов для выбора.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "103890088"
---
# <a name="overrideeapcertificateselection"></a><span data-ttu-id="aa3ad-103">оверридиапцертификатеселектион</span><span class="sxs-lookup"><span data-stu-id="aa3ad-103">OverrideEAPCertificateSelection</span></span>

<span data-ttu-id="aa3ad-104">Раздел реестра Оверридиапцертификатеселектион определяет, будет ли клиент переопределять поведение выбора сертификата смарт-карты по умолчанию и предоставлять пользователю больше сертификатов для выбора.</span><span class="sxs-lookup"><span data-stu-id="aa3ad-104">The OverrideEAPCertificateSelection registry key determines whether the client will override the default smart card certificate selection behavior and provide the user with more certificates to choose from.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="aa3ad-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="aa3ad-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a><span data-ttu-id="aa3ad-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa3ad-106">Remarks</span></span>

<span data-ttu-id="aa3ad-107">Это **\_ двоичное значение reg** .</span><span class="sxs-lookup"><span data-stu-id="aa3ad-107">This is a **REG\_BINARY** value.</span></span>



| <span data-ttu-id="aa3ad-108">Значение</span><span class="sxs-lookup"><span data-stu-id="aa3ad-108">Value</span></span> | <span data-ttu-id="aa3ad-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aa3ad-109">Description</span></span>                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa3ad-110">0x000</span><span class="sxs-lookup"><span data-stu-id="aa3ad-110">0x000</span></span> | <span data-ttu-id="aa3ad-111">Не переопределяйте поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa3ad-111">Do not override the default behavior.</span></span>                                                                                                                                                                |
| <span data-ttu-id="aa3ad-112">0x001</span><span class="sxs-lookup"><span data-stu-id="aa3ad-112">0x001</span></span> | <span data-ttu-id="aa3ad-113">Выберите последний подключенный сертификат из смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="aa3ad-113">Choose the last attached certificate from the smart card.</span></span>                                                                                                                                            |
| <span data-ttu-id="aa3ad-114">0x010</span><span class="sxs-lookup"><span data-stu-id="aa3ad-114">0x010</span></span> | <span data-ttu-id="aa3ad-115">Показывает все сертификаты в пользовательском интерфейсе выбора сертификата из смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="aa3ad-115">Shows all certificates in the certificate selection UI from the smart card.</span></span>                                                                                                                          |
| <span data-ttu-id="aa3ad-116">0x100</span><span class="sxs-lookup"><span data-stu-id="aa3ad-116">0x100</span></span> | <span data-ttu-id="aa3ad-117">Показывает все сертификаты в пользовательском интерфейсе выбора сертификата из реестра.</span><span class="sxs-lookup"><span data-stu-id="aa3ad-117">Shows all certificates in the certificate selection UI from the registry.</span></span>                                                                                                                            |
| <span data-ttu-id="aa3ad-118">0x101</span><span class="sxs-lookup"><span data-stu-id="aa3ad-118">0x101</span></span> | <span data-ttu-id="aa3ad-119">Показывает все сертификаты в пользовательском интерфейсе выбора сертификата из реестра и последнего присоединенного сертификата со смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="aa3ad-119">Shows all certificates in the certificate selection UI from the registry and the last attached certificate from the smart card.</span></span> <span data-ttu-id="aa3ad-120">Отображает последний присоединенный сертификат из смарт-карты, как выбрано.</span><span class="sxs-lookup"><span data-stu-id="aa3ad-120">Shows the last attached certificate from the smart card as selected.</span></span> |
| <span data-ttu-id="aa3ad-121">0x110</span><span class="sxs-lookup"><span data-stu-id="aa3ad-121">0x110</span></span> | <span data-ttu-id="aa3ad-122">Показывает все сертификаты в пользовательском интерфейсе выбора сертификата из реестра и смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="aa3ad-122">Shows all certificates in the certificate selection UI from the registry and the smart card.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="aa3ad-123">См. также</span><span class="sxs-lookup"><span data-stu-id="aa3ad-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa3ad-124">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="aa3ad-124">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




