---
title: Порт 3 устарел для драйверов NDIS 6,30
description: Порт 3 устарел для драйверов NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104488409"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a><span data-ttu-id="fb29f-103">Порт 3 устарел для драйверов NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="fb29f-103">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="fb29f-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="fb29f-104">Platforms</span></span>

<span data-ttu-id="fb29f-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="fb29f-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="fb29f-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb29f-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="fb29f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fb29f-107">Description</span></span>

<span data-ttu-id="fb29f-108">Windows 8 устраняет поддержку платформы для драйверов WLAN минипорта NDIS для создания или запуска порта расширяемости IHV (также известного как третий порт).</span><span class="sxs-lookup"><span data-stu-id="fb29f-108">Windows 8 removes platform support for NDIS miniport WLAN drivers to create or start up the IHV extensibility port (also known as 3rd port).</span></span> <span data-ttu-id="fb29f-109">Эта функция появилась в Windows 7 как мера промежуточного, а Wi-Fi Alliance (ВФА) разработала спецификацию Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="fb29f-109">This feature was introduced in Windows 7 as a stopgap measure while the Wi-Fi Alliance (WFA) developed the Wi-Fi Direct specification.</span></span> <span data-ttu-id="fb29f-110">Теперь спецификация завершена, продукты, использующие Wi-Fi Direct, сертифицированы, а в Windows 8 появился собственный стек Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="fb29f-110">The specification is now finished, products using Wi-Fi Direct are being certified, and Windows 8 introduces a native Wi-Fi Direct stack.</span></span>

## <a name="manifestation"></a><span data-ttu-id="fb29f-111">Проявление</span><span class="sxs-lookup"><span data-stu-id="fb29f-111">Manifestation</span></span>

<span data-ttu-id="fb29f-112">Ничто не так, так как третий порт является возможностью платформы, которая запускается драйверами минипорта WLAN, если они необходимы.</span><span class="sxs-lookup"><span data-stu-id="fb29f-112">Nothing, as third port is a platform capability that WLAN miniport drivers start up if they need this functionality.</span></span>

## <a name="solution"></a><span data-ttu-id="fb29f-113">Решение</span><span class="sxs-lookup"><span data-stu-id="fb29f-113">Solution</span></span>

<span data-ttu-id="fb29f-114">Функция порта расширяемости доступна для существующих драйверов, не сообщающих NDIS 6,30 для обеспечения совместимости устройств.</span><span class="sxs-lookup"><span data-stu-id="fb29f-114">We are keeping the extensibility port feature available for existing drivers that do not report NDIS 6.30 to maintain device compatibility.</span></span> <span data-ttu-id="fb29f-115">Однако новые драйверы WLAN, сообщающие о выпуске NDIS 6,30, не смогут запустить этот порт. Вместо этого разработчики этих драйверов должны использовать Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="fb29f-115">However, new WLAN drivers that report NDIS 6.30 will not be able to start this port; instead, developers of these drivers should use Wi-Fi Direct.</span></span>

 

 




