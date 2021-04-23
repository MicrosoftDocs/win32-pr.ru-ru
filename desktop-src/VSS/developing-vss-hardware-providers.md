---
description: Поставщики оборудования реализуют интерфейсы Ивсспровидеркреатеснапшотсет и Ивсшардвареснапшотпровидер.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Разработка поставщиков оборудования VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272587"
---
# <a name="developing-vss-hardware-providers"></a><span data-ttu-id="70447-103">Разработка поставщиков оборудования VSS</span><span class="sxs-lookup"><span data-stu-id="70447-103">Developing VSS Hardware Providers</span></span>

<span data-ttu-id="70447-104">Поставщики оборудования реализуют интерфейсы [**ивсспровидеркреатеснапшотсет**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) и [**ивсшардвареснапшотпровидер**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) .</span><span class="sxs-lookup"><span data-stu-id="70447-104">Hardware providers implement the [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) and [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) interfaces.</span></span> <span data-ttu-id="70447-105">**Ивсспровидеркреатеснапшотсет** реализует виртуализацию состояния теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="70447-105">**IVssProviderCreateSnapshotSet** implements the shadow copy state sequencing.</span></span> <span data-ttu-id="70447-106">**Ивсшардвареснапшотпровидер** работает с абстракцией LUN.</span><span class="sxs-lookup"><span data-stu-id="70447-106">**IVssHardwareSnapshotProvider** operates on a LUN abstraction.</span></span> <span data-ttu-id="70447-107">Поставщики должны быть реализованы как внутрипроцессный COM-сервер.</span><span class="sxs-lookup"><span data-stu-id="70447-107">Providers must be implemented as an out-of-process COM server.</span></span> <span data-ttu-id="70447-108">Поставщики используют специфические для поставщика механизмы (как правило, частные IOCTL) для взаимодействия с подсистемой хранения, создающей экземпляры LUN теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="70447-108">Providers use provider-specific mechanisms (often private IOCTLs) to communicate with the storage subsystem that instantiates the shadow copy LUNs.</span></span>

-   [<span data-ttu-id="70447-109">Регистрация и загрузка поставщика теневого копирования</span><span class="sxs-lookup"><span data-stu-id="70447-109">Shadow Copy Provider Registration and Loading</span></span>](shadow-copy-provider-registration-and-loading.md)
-   [<span data-ttu-id="70447-110">Создание теневых копий для поставщиков</span><span class="sxs-lookup"><span data-stu-id="70447-110">Shadow Copy Creation for Providers</span></span>](shadow-copy-creation-for-providers.md)
-   [<span data-ttu-id="70447-111">Взаимодействие и поведение поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="70447-111">Hardware Provider Interactions and Behaviors</span></span>](hardware-provider-interactions-and-behaviors.md)

 

 



