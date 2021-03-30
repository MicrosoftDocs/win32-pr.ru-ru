---
title: Повторное распространение проигрывателя Windows Media 10
description: Повторное распространение проигрывателя Windows Media 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773445"
---
# <a name="redistributing-windows-media-player-10"></a><span data-ttu-id="5749e-103">Повторное распространение проигрывателя Windows Media 10</span><span class="sxs-lookup"><span data-stu-id="5749e-103">Redistributing Windows Media Player 10</span></span>

<span data-ttu-id="5749e-104">Проигрыватель Windows Media Player 10 можно установить в Windows XP с помощью следующей программы установки.</span><span class="sxs-lookup"><span data-stu-id="5749e-104">You can install Windows Media Player 10 on Windows XP by using the following setup program.</span></span>

-   <span data-ttu-id="5749e-105">MP10Setup.exe</span><span class="sxs-lookup"><span data-stu-id="5749e-105">MP10Setup.exe</span></span>

<span data-ttu-id="5749e-106">Ниже приведен пример командной строки для установки без пользовательского интерфейса и запроса перезагрузки или перезапуска.</span><span class="sxs-lookup"><span data-stu-id="5749e-106">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="5749e-107">В следующей таблице приведены дополнительные параметры, которые можно использовать с программой установки проигрывателя Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="5749e-107">The following table shows additional parameters that you can use with the Windows Media Player 10 setup program.</span></span>



| <span data-ttu-id="5749e-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5749e-108">Parameter</span></span>              | <span data-ttu-id="5749e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5749e-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5749e-110">/номиграте</span><span class="sxs-lookup"><span data-stu-id="5749e-110">/NoMigrate</span></span>             | <span data-ttu-id="5749e-111">Предотвращение миграции библиотек.</span><span class="sxs-lookup"><span data-stu-id="5749e-111">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5749e-112">/нестедресторе</span><span class="sxs-lookup"><span data-stu-id="5749e-112">/NestedRestore</span></span>         | <span data-ttu-id="5749e-113">Создайте вложенную точку восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="5749e-113">Create a nested system restore point.</span></span> <span data-ttu-id="5749e-114">Используйте этот параметр, если приложение создает точку восстановления системы для вложения точки восстановления проигрывателя Windows Media в точку восстановления приложения.</span><span class="sxs-lookup"><span data-stu-id="5749e-114">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5749e-115">/дисалловсистемресторе</span><span class="sxs-lookup"><span data-stu-id="5749e-115">/DisallowSystemRestore</span></span> | <span data-ttu-id="5749e-116">Запретить создание точки восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="5749e-116">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="5749e-117">Этот флаг отключит создание точки восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="5749e-117">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="5749e-118">В большинстве случаев этот флаг не следует использовать для общего распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="5749e-118">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="5749e-119">Его следует использовать только в том случае, если вы можете явно выбрать от имени конечного пользователя не поддерживать откат файлов проигрывателя Windows Media до более ранней версии проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="5749e-119">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="5749e-120">Этот флаг следует использовать только для корпоративного развертывания или установки изготовителя оборудования (OEM).</span><span class="sxs-lookup"><span data-stu-id="5749e-120">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="5749e-121">/дефаултсервице</span><span class="sxs-lookup"><span data-stu-id="5749e-121">/DefaultService</span></span>        | <span data-ttu-id="5749e-122">Задайте начальное Интернет-хранилище.</span><span class="sxs-lookup"><span data-stu-id="5749e-122">Set the initial online store.</span></span> <span data-ttu-id="5749e-123">Дополнительные сведения см. в статье [Параметры командной строки программы установки для Интернет-магазинов](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="5749e-123">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="5749e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="5749e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5749e-125">**Распространение программного обеспечения проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5749e-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> <dt>

[<span data-ttu-id="5749e-126">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="5749e-126">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




