---
title: СторахЦи заменяет МСАХЦИ
description: СторахЦи заменяет МСАХЦИ
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "105700961"
---
# <a name="storahci-replaces-msahci"></a><span data-ttu-id="f9da1-103">СторахЦи заменяет МСАХЦИ</span><span class="sxs-lookup"><span data-stu-id="f9da1-103">StorAHCI replaces MSAHCI</span></span>

## <a name="platforms"></a><span data-ttu-id="f9da1-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="f9da1-104">Platforms</span></span>

<span data-ttu-id="f9da1-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="f9da1-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="f9da1-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9da1-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="f9da1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f9da1-107">Description</span></span>

<span data-ttu-id="f9da1-108">СторахЦи, Минипорт Storport, поддерживает контроллеры интерфейса AHCI с последовательным подключением (SATA) в Windows и заменяет МСАХЦИ, Мини-порт Атапорт.</span><span class="sxs-lookup"><span data-stu-id="f9da1-108">StorAHCI, a Storport miniport, supports serial advanced technology attachment (SATA) advanced host controller interface (AHCI) controllers in Windows, and replaces MSAHCI, an ATAport miniport.</span></span>

## <a name="manifestation"></a><span data-ttu-id="f9da1-109">Проявление</span><span class="sxs-lookup"><span data-stu-id="f9da1-109">Manifestation</span></span>

<span data-ttu-id="f9da1-110">В функциональности или производительности не должно быть изменений; Этот драйвер поддерживает все устройства, которые поддерживает МСАХЦИ.</span><span class="sxs-lookup"><span data-stu-id="f9da1-110">There should be no change in functionality or performance; this driver supports all the same devices that MSAHCI supports.</span></span>

<span data-ttu-id="f9da1-111">Это изменение прозрачно для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f9da1-111">This change is transparent to the user.</span></span>

## <a name="mitigation"></a><span data-ttu-id="f9da1-112">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="f9da1-112">Mitigation</span></span>

<span data-ttu-id="f9da1-113">Обновите все служебные программы и скрипты, использующие привязки Атапорт.</span><span class="sxs-lookup"><span data-stu-id="f9da1-113">Update any utilities and scripts that rely on ATAport bindings.</span></span> <span data-ttu-id="f9da1-114">Не полагайтесь на имя диска.</span><span class="sxs-lookup"><span data-stu-id="f9da1-114">Do not rely on the drive name.</span></span> <span data-ttu-id="f9da1-115">Вместо этого используйте обнаружение дисков стандартного типа.</span><span class="sxs-lookup"><span data-stu-id="f9da1-115">Instead use standard disk detection.</span></span>

 

 




