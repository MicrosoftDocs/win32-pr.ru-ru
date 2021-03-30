---
title: Повторное распространение проигрывателя Windows Media 11
description: Повторное распространение проигрывателя Windows Media 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067748"
---
# <a name="redistributing-windows-media-player-11"></a><span data-ttu-id="c0d0f-103">Повторное распространение проигрывателя Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="c0d0f-103">Redistributing Windows Media Player 11</span></span>

<span data-ttu-id="c0d0f-104">Windows Media Player 11 можно установить в Windows XP с помощью одной из следующих программ установки, где *LocaleID* — это идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-104">You can install Windows Media Player 11 on Windows XP by using one of the following setup programs, where *localeId* is a locale identifier.</span></span>

-   <span data-ttu-id="c0d0f-105">WMP11-WindowsXP-x86-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="c0d0f-105">wmp11-windowsxp-x86-*localeId*.exe</span></span>
-   <span data-ttu-id="c0d0f-106">WMP11-WindowsXP-x64-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="c0d0f-106">wmp11-windowsxp-x64-*localeId*.exe</span></span>

<span data-ttu-id="c0d0f-107">Ниже приведен пример командной строки для установки без пользовательского интерфейса и запроса перезагрузки или перезапуска.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-107">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="c0d0f-108">В следующей таблице приведены дополнительные параметры, которые можно использовать с программой установки проигрывателя Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-108">The following table shows additional parameters that you can use with the Windows Media Player 11 setup program.</span></span>



| <span data-ttu-id="c0d0f-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="c0d0f-109">Parameter</span></span>              | <span data-ttu-id="c0d0f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c0d0f-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d0f-111">/номиграте</span><span class="sxs-lookup"><span data-stu-id="c0d0f-111">/NoMigrate</span></span>             | <span data-ttu-id="c0d0f-112">Предотвращение миграции библиотек.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-112">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c0d0f-113">/нестедресторе</span><span class="sxs-lookup"><span data-stu-id="c0d0f-113">/NestedRestore</span></span>         | <span data-ttu-id="c0d0f-114">Создайте вложенную точку восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-114">Create a nested system restore point.</span></span> <span data-ttu-id="c0d0f-115">Используйте этот параметр, если приложение создает точку восстановления системы для вложения точки восстановления проигрывателя Windows Media в точку восстановления приложения.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-115">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c0d0f-116">/дисалловсистемресторе</span><span class="sxs-lookup"><span data-stu-id="c0d0f-116">/DisallowSystemRestore</span></span> | <span data-ttu-id="c0d0f-117">Запретить создание точки восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-117">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="c0d0f-118">Этот флаг отключит создание точки восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-118">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="c0d0f-119">В большинстве случаев этот флаг не следует использовать для общего распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-119">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="c0d0f-120">Его следует использовать только в том случае, если вы можете явно выбрать от имени конечного пользователя не поддерживать откат файлов проигрывателя Windows Media до более ранней версии проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-120">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="c0d0f-121">Этот флаг следует использовать только для корпоративного развертывания или установки изготовителя оборудования (OEM).</span><span class="sxs-lookup"><span data-stu-id="c0d0f-121">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="c0d0f-122">/дефаултсервице</span><span class="sxs-lookup"><span data-stu-id="c0d0f-122">/DefaultService</span></span>        | <span data-ttu-id="c0d0f-123">Задайте начальное Интернет-хранилище.</span><span class="sxs-lookup"><span data-stu-id="c0d0f-123">Set the initial online store.</span></span> <span data-ttu-id="c0d0f-124">Дополнительные сведения см. в статье [Параметры командной строки программы установки для Интернет-магазинов](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="c0d0f-124">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="c0d0f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c0d0f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0d0f-126">**Распространение программного обеспечения проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c0d0f-126">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




