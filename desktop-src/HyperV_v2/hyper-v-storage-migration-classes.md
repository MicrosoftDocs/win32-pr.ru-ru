---
description: API миграции Hyper-V определяет следующие элементы программирования.
ms.assetid: E1FE7351-2F14-4C8F-AF5C-9009CC61CE22
title: Справочник по API миграции Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a05bc976cf1722aba558eeca9c7b04cdf7287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683109"
---
# <a name="hyper-v-migration-api-reference"></a><span data-ttu-id="58f78-103">Справочник по API миграции Hyper-V</span><span class="sxs-lookup"><span data-stu-id="58f78-103">Hyper-V migration API reference</span></span>

<span data-ttu-id="58f78-104">API миграции Hyper-V определяет следующие элементы программирования.</span><span class="sxs-lookup"><span data-stu-id="58f78-104">The Hyper-V migration API defines the following programming elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58f78-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="58f78-105">In this section</span></span>



| <span data-ttu-id="58f78-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="58f78-106">Topic</span></span>                                                                                                                                | <span data-ttu-id="58f78-107">Описание</span><span class="sxs-lookup"><span data-stu-id="58f78-107">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58f78-108">**Мсвм \_ мигратионжоб**</span><span class="sxs-lookup"><span data-stu-id="58f78-108">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)<br/>                                                                           | <span data-ttu-id="58f78-109">Этот класс представляет задание операции миграции, созданное для миграции хранилища или виртуальной системы с помощью службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="58f78-109">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span><br/>                                                 |
| [<span data-ttu-id="58f78-110">**Мсвм \_ виртуалсистеммигратионкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="58f78-110">**Msvm\_VirtualSystemMigrationCapabilities**</span></span>](msvm-virtualsystemmigrationcapabilities.md)<br/>                               | <span data-ttu-id="58f78-111">Определяет средства, с помощью которых клиент может обнаружить методы, предоставляемые службой миграции, и допустимый диапазон данных параметров миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="58f78-111">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span><br/>                                |
| [<span data-ttu-id="58f78-112">**Мсвм \_ виртуалсистеммигратионнетворксеттингдата**</span><span class="sxs-lookup"><span data-stu-id="58f78-112">**Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>](msvm-virtualsystemmigrationnetworksettingdata.md)<br/>                   | <span data-ttu-id="58f78-113">Представляет сеть, в которой служба миграции виртуальной системы прослушивает входящую миграцию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="58f78-113">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span><br/>                                                                 |
| [<span data-ttu-id="58f78-114">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="58f78-114">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)<br/>                                         | <span data-ttu-id="58f78-115">Представляет службу миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="58f78-115">Represents the virtual system migration service.</span></span> <span data-ttu-id="58f78-116">Он используется для миграции виртуальной системы или для переноса хранилища виртуальной системы с одной платформы виртуализации в другую.</span><span class="sxs-lookup"><span data-stu-id="58f78-116">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span><br/> |
| [<span data-ttu-id="58f78-117">**Мсвм \_ виртуалсистеммигратионсервицесеттингдата**</span><span class="sxs-lookup"><span data-stu-id="58f78-117">**Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>](msvm-virtualsystemmigrationservicesettingdata.md)<br/>                   | <span data-ttu-id="58f78-118">Представляет параметры для службы миграции виртуальной системы на узле.</span><span class="sxs-lookup"><span data-stu-id="58f78-118">Represents the settings for the virtual system migration service on a host.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="58f78-119">**Мсвм \_ виртуалсистеммигратионсервицесеттингдатакомпонент**</span><span class="sxs-lookup"><span data-stu-id="58f78-119">**Msvm\_VirtualSystemMigrationServiceSettingDataComponent**</span></span>](msvm-virtualsystemmigrationservicesettingdatacomponent.md)<br/> | <span data-ttu-id="58f78-120">Ассоциация, используемая для представления параметров сети миграции виртуальной системы для службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="58f78-120">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span><br/>                                                                      |
| [<span data-ttu-id="58f78-121">**Мсвм \_ виртуалсистеммигратионсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="58f78-121">**Msvm\_VirtualSystemMigrationSettingData**</span></span>](msvm-virtualsystemmigrationsettingdata.md)<br/>                                 | <span data-ttu-id="58f78-122">Представляет параметры миграции для миграции виртуальной системы и хранилища, подключенного к виртуальной системе.</span><span class="sxs-lookup"><span data-stu-id="58f78-122">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span><br/>                                                                           |



 

 

 




