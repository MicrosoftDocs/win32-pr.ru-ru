---
title: Объект агента отзыва лицензий
description: Объект агента отзыва лицензий
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Пакет SDK для Windows Media Format, объекты агента отзыва лицензий
- Расширенный формат систем (ASF), объекты агента отзыва лицензий
- ASF (Расширенный системный формат), объекты агента отзыва лицензий
- объекты, объекты агента отзыва лицензий
- Отзыв лицензий, объекты агента отзыва лицензий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412485"
---
# <a name="license-revocation-agent-object"></a><span data-ttu-id="ad949-108">Объект агента отзыва лицензий</span><span class="sxs-lookup"><span data-stu-id="ad949-108">License Revocation Agent Object</span></span>

<span data-ttu-id="ad949-109">Объект агента отзыва лицензий управляет клиентской стороны отзыва лицензий.</span><span class="sxs-lookup"><span data-stu-id="ad949-109">The license revocation agent object manages the client side of license revocation.</span></span> <span data-ttu-id="ad949-110">Отзыв лицензий — это процесс, с помощью которого сервер лицензирования может удалить лицензии из хранилища лицензий на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="ad949-110">License revocation is the process by which a license server can remove licenses from the license store on the client computer.</span></span> <span data-ttu-id="ad949-111">Процесс включает в себя передачу нескольких сообщений между клиентским приложением и сервером лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ad949-111">The process involves passing several messages between the client application and the license server.</span></span> <span data-ttu-id="ad949-112">Методы, предоставляемые в этом объекте, и создают эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad949-112">The methods exposed on this object process and generate those messages.</span></span>

<span data-ttu-id="ad949-113">Объект агента отзыва лицензий создается функцией [**вмкреателиценсеревокатионажент**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , которая устанавливает указатель на интерфейс [**ивмлиценсеревокатионажент**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="ad949-113">The license revocation agent object is created by the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function, which sets a pointer to an [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span> <span data-ttu-id="ad949-114">**IUnknown** и **ивмлиценсеревокатионажент** — это единственные интерфейсы, поддерживаемые этим объектом.</span><span class="sxs-lookup"><span data-stu-id="ad949-114">**IUnknown** and **IWMLicenseRevocationAgent** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad949-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ad949-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad949-116">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="ad949-116">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




