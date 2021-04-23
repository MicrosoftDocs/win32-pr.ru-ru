---
description: Виртуальная BIOS — это образ программного обеспечения, который загружается в ОЗУ для настройки некоторых основных аспектов и загрузки компьютерной системы. Имеется один элемент BIOS на компьютерную систему, и этот элемент нельзя заменить или удалить.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Классы BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998564"
---
# <a name="bios-classes"></a><span data-ttu-id="23b5f-104">Классы BIOS</span><span class="sxs-lookup"><span data-stu-id="23b5f-104">BIOS classes</span></span>

<span data-ttu-id="23b5f-105">Виртуальная BIOS — это образ программного обеспечения, который загружается в ОЗУ для настройки некоторых основных аспектов и загрузки компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="23b5f-105">The virtual BIOS is a software image that is loaded into RAM to configure some of the basic aspects of and boot a computer system.</span></span> <span data-ttu-id="23b5f-106">Имеется один элемент BIOS на компьютерную систему, и этот элемент нельзя заменить или удалить.</span><span class="sxs-lookup"><span data-stu-id="23b5f-106">There is one BIOS element per computer system and that element cannot be replaced or removed.</span></span> <span data-ttu-id="23b5f-107">Таким словами, пул ресурсов для добавления новых элементов BIOS в виртуальную машину отсутствует.</span><span class="sxs-lookup"><span data-stu-id="23b5f-107">Thus, there is no resource pool for adding new BIOS elements to the virtual machine.</span></span> <span data-ttu-id="23b5f-108">Элемент BIOS также не имеет собственного класса SettingData для описания параметров BIOS.</span><span class="sxs-lookup"><span data-stu-id="23b5f-108">The BIOS element also does not have its own SettingData class to describe the settings for the BIOS.</span></span> <span data-ttu-id="23b5f-109">Параметры BIOS, такие как серийные номера, порядок загрузки и состояние NUM LOCK, находятся в классе [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="23b5f-109">Settings for the BIOS, such as serial numbers, boot order, and num lock state, are found in the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span>

<span data-ttu-id="23b5f-110">Ниже перечислены классы WMI виртуализации, связанные с BIOS.</span><span class="sxs-lookup"><span data-stu-id="23b5f-110">The following are virtualization WMI classes related to the BIOS.</span></span> <span data-ttu-id="23b5f-111">Эти классы находятся в \\ \\ . \\ Корневое \\ пространство имен виртуализации.</span><span class="sxs-lookup"><span data-stu-id="23b5f-111">These classes are in the \\\\.\\Root\\Virtualization namespace.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="23b5f-112">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="23b5f-112">In this section</span></span>



| <span data-ttu-id="23b5f-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="23b5f-113">Topic</span></span>                                                    | <span data-ttu-id="23b5f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="23b5f-114">Description</span></span>                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23b5f-115">**Мсвм \_ биоселемент**</span><span class="sxs-lookup"><span data-stu-id="23b5f-115">**Msvm\_BIOSElement**</span></span>](msvm-bioselement.md)<br/> | <span data-ttu-id="23b5f-116">Представляет программное обеспечение низкого уровня, которое загружается в ОЗУ для настройки и запуска системы.</span><span class="sxs-lookup"><span data-stu-id="23b5f-116">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span><br/> |
| [<span data-ttu-id="23b5f-117">**Мсвм \_ систембиос**</span><span class="sxs-lookup"><span data-stu-id="23b5f-117">**Msvm\_SystemBIOS**</span></span>](msvm-systembios.md)<br/>   | <span data-ttu-id="23b5f-118">Используется для связывания виртуальной машины с BIOS.</span><span class="sxs-lookup"><span data-stu-id="23b5f-118">Used to associate a virtual machine with its BIOS.</span></span><br/>                                           |



 

 

 




