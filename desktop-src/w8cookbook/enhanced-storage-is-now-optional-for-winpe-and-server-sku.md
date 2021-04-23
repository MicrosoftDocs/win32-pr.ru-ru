---
title: Расширенное хранилище теперь является необязательным для WINPE и SKU сервера.
description: Расширенное хранилище теперь является необязательным для WINPE и SKU сервера.
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104339425"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a><span data-ttu-id="1e7f5-103">Расширенное хранилище теперь является необязательным для WINPE и SKU сервера.</span><span class="sxs-lookup"><span data-stu-id="1e7f5-103">Enhanced storage is now optional for WINPE and server SKU</span></span>

## <a name="platforms"></a><span data-ttu-id="1e7f5-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="1e7f5-104">Platforms</span></span>

<span data-ttu-id="1e7f5-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="1e7f5-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="1e7f5-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e7f5-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="1e7f5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1e7f5-107">Description</span></span>

<span data-ttu-id="1e7f5-108">Расширенное хранилище всегда было доступно в USB-устройствах Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e7f5-108">Enhanced storage was always available in Windows 7 USB devices.</span></span> <span data-ttu-id="1e7f5-109">С выпуском Windows 8 он доступен для всех запоминающих устройств.</span><span class="sxs-lookup"><span data-stu-id="1e7f5-109">With the release of Windows 8, it is available for all storage devices.</span></span> <span data-ttu-id="1e7f5-110">На клиентских устройствах оно включено по умолчанию. в серверных устройствах это необязательно и должно быть подготовлено с помощью среда предустановки Windows (WinPE).</span><span class="sxs-lookup"><span data-stu-id="1e7f5-110">In client-based devices, it is enabled by default; in server devices it is optional and must be provisioned through Windows Preinstallation Environment (WinPE).</span></span>

## <a name="manifestation"></a><span data-ttu-id="1e7f5-111">Проявление</span><span class="sxs-lookup"><span data-stu-id="1e7f5-111">Manifestation</span></span>

<span data-ttu-id="1e7f5-112">Серверное устройство завершится ошибкой, если не включено Расширенное хранилище.</span><span class="sxs-lookup"><span data-stu-id="1e7f5-112">The server device will fail if enhanced storage is not enabled.</span></span>

<span data-ttu-id="1e7f5-113">Загрузочные устройства должны быть подготовлены с помощью WinPE, если этот параметр включен.</span><span class="sxs-lookup"><span data-stu-id="1e7f5-113">Boot devices must be provisioned through WinPE with this enabled.</span></span>

## <a name="solution"></a><span data-ttu-id="1e7f5-114">Решение</span><span class="sxs-lookup"><span data-stu-id="1e7f5-114">Solution</span></span>

<span data-ttu-id="1e7f5-115">Поскольку Расширенное хранилище является необязательным для сервера среды выполнения, разработчики должны добавить его в WinPE для подготовки и активации этих дисков.</span><span class="sxs-lookup"><span data-stu-id="1e7f5-115">Because enhanced storage is optional for runtime server, developers must add it to WinPE for provisioning and activation of those drives.</span></span> <span data-ttu-id="1e7f5-116">Дополнительные сведения см. в разделе рекомендации по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="1e7f5-116">See the deployment guide for details.</span></span>

<span data-ttu-id="1e7f5-117">Администраторы сервера должны явно настроить сервер для использования расширенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="1e7f5-117">Server administrators must then explicitly configure their server to use enhanced storage.</span></span>

 

 




