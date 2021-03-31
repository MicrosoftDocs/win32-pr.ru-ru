---
title: Сохраняемость конфигурации
description: Сохраняемость конфигурации
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK, сохраняемость
- Пакет SDK для формата Windows Media, сохранение конфигурации
- Расширенный формат систем (ASF), сохраняемость
- ASF (Расширенный системный формат), сохраняемость
- Расширенный формат систем (ASF), сохранение конфигурации
- ASF (Расширенный системный формат), сохранение конфигурации
- сохраняемость конфигурации
- сохранение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412567"
---
# <a name="configuration-persistence"></a><span data-ttu-id="5452b-111">Сохраняемость конфигурации</span><span class="sxs-lookup"><span data-stu-id="5452b-111">Configuration Persistence</span></span>

<span data-ttu-id="5452b-112">Ни одно из свойств, доступных для записи, описанных в этой документации, не сохраняется пакетом Windows Media SDK.</span><span class="sxs-lookup"><span data-stu-id="5452b-112">None of the write-enabled properties described in this documentation are saved by the Windows Media SDK.</span></span> <span data-ttu-id="5452b-113">Каждое приложение, использующее пакет SDK, должно предоставлять собственные процедуры сохранения при необходимости и вызывать соответствующий метод Set для каждого экземпляра пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="5452b-113">Each application that uses the SDK must provide its own persistence procedures as needed and invoke the appropriate set method upon each instance of the SDK.</span></span> <span data-ttu-id="5452b-114">Таким образом, изменения конфигурации, вносимые одним приложением, не влияют на другое приложение.</span><span class="sxs-lookup"><span data-stu-id="5452b-114">In this way, configuration changes made by one application do not affect another application.</span></span> <span data-ttu-id="5452b-115">Например, изменение времени буферизации в одном проигрывателе не влияет на другой игрок.</span><span class="sxs-lookup"><span data-stu-id="5452b-115">For example, changing the buffering time in one player does not affect another player.</span></span>

<span data-ttu-id="5452b-116">Единственным исключением из этого правила является информация об учетных данных.</span><span class="sxs-lookup"><span data-stu-id="5452b-116">The one exception to this rule is for the credentials information.</span></span> <span data-ttu-id="5452b-117">Если приложение указывает, что при возвращении из вызова **аккуирекредентиалс** необходимо сохранить сведения об идентификаторе пользователя и пароле, пакет SDK сохранит эти сведения.</span><span class="sxs-lookup"><span data-stu-id="5452b-117">If the application indicates, in its return from the **AcquireCredentials** call, that the user ID and password information must be persisted, the SDK saves this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5452b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5452b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5452b-119">**Реализация функций сети**</span><span class="sxs-lookup"><span data-stu-id="5452b-119">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="5452b-120">**Интерфейс Ивмкредентиалкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="5452b-120">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




