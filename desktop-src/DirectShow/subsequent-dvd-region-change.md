---
description: Изменение следующего региона DVD
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Изменение следующего региона DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674271"
---
# <a name="subsequent-dvd-region-change"></a><span data-ttu-id="db9b8-103">Изменение следующего региона DVD</span><span class="sxs-lookup"><span data-stu-id="db9b8-103">Subsequent DVD Region Change</span></span>

<span data-ttu-id="db9b8-104">В Windows 2000 и более поздних версиях Навигатор DVD вызывает страницу свойств устройства DVD-ROM в диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="db9b8-104">In Windows 2000 and later, the DVD Navigator invokes a property page on the DVD-ROM drive device in the Device Manager.</span></span> <span data-ttu-id="db9b8-105">Эта страница свойств также выдается приложением DVDPlay.exe, когда необходимо изменить регион.</span><span class="sxs-lookup"><span data-stu-id="db9b8-105">This property page is also brought up by the DVDPlay.exe application when a region needs to be changed.</span></span> <span data-ttu-id="db9b8-106">Пользовательский интерфейс этой страницы свойств очень похож на DVDRgn.exe и является региональным в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="db9b8-106">The UI of this property page is very similar to that of DVDRgn.exe and it is regionalized in the operating system.</span></span>

<span data-ttu-id="db9b8-107">Для дисков RPC1 компоненты операционной системы Windows управляют изменениями в регионах.</span><span class="sxs-lookup"><span data-stu-id="db9b8-107">For RPC1 drives, the Windows Operating System components manage region changes.</span></span> <span data-ttu-id="db9b8-108">RPC2 диски поддерживают настройку региона на своем оборудовании.</span><span class="sxs-lookup"><span data-stu-id="db9b8-108">RPC2 drives maintain the region setting in their own hardware.</span></span> <span data-ttu-id="db9b8-109">Если количество допустимых изменений на RPC2 диске исчерпано, диск не сможет вызвать изменение региона, а компонент изменения региона в операционной системе сообщит пользователю.</span><span class="sxs-lookup"><span data-stu-id="db9b8-109">When the number of allowed changes are exhausted on a RPC2 drive, the drive will fail the call to change the region and the region-change component in the operating system will indicate that to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db9b8-110">См. также</span><span class="sxs-lookup"><span data-stu-id="db9b8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db9b8-111">Поддержка смены региона DVD в Windows</span><span class="sxs-lookup"><span data-stu-id="db9b8-111">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



