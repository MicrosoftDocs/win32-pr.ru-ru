---
description: Функция DeviceIoControl предоставляет интерфейс управления входными и выходными данными устройства (IOCTL), с помощью которого приложение может напрямую взаимодействовать с драйвером устройства.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Входные и выходные элементы устройства (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896254"
---
# <a name="device-input-and-output-control-ioctl"></a><span data-ttu-id="e3a6d-103">Входные и выходные элементы устройства (IOCTL)</span><span class="sxs-lookup"><span data-stu-id="e3a6d-103">Device Input and Output Control (IOCTL)</span></span>

<span data-ttu-id="e3a6d-104">Функция [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) предоставляет интерфейс управления входными и выходными данными устройства (IOCTL), с помощью которого приложение может напрямую взаимодействовать с драйвером устройства.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-104">The [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function provides a device input and output control (IOCTL) interface through which an application can communicate directly with a device driver.</span></span> <span data-ttu-id="e3a6d-105">Функция **DeviceIoControl** — это интерфейс общего назначения, который может передавать управляющие коды различным устройствам.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-105">The **DeviceIoControl** function is a general-purpose interface that can send control codes to a variety of devices.</span></span> <span data-ttu-id="e3a6d-106">Каждый управляющий код представляет операцию, которую должен выполнить драйвер.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-106">Each control code represents an operation for the driver to perform.</span></span> <span data-ttu-id="e3a6d-107">Например, управляющий код может попросить драйверу устройства вернуть сведения о соответствующем устройстве или направить драйвер для выполнения действия на устройстве, например для форматирования диска.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-107">For example, a control code can ask a device driver to return information about the corresponding device, or direct the driver to carry out an action on the device, such as formatting a disk.</span></span>

<span data-ttu-id="e3a6d-108">В файлах заголовков SDK определен ряд стандартных управляющих кодов.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-108">A number of standard control codes are defined in the SDK header files.</span></span> <span data-ttu-id="e3a6d-109">Кроме того, драйверы устройств могут определять собственные управляющие коды для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-109">In addition, device drivers can define their own device-specific control codes.</span></span> <span data-ttu-id="e3a6d-110">Список стандартных кодов управления, входящих в документацию по пакету SDK, см. в разделе "Примечания" для [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span><span class="sxs-lookup"><span data-stu-id="e3a6d-110">For a list of standard control codes included in the SDK documentation, see the Remarks section of [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span></span>

<span data-ttu-id="e3a6d-111">Типы управляющих кодов, которые можно указать, зависят от устройства, к которому осуществляется доступ, и от платформы, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-111">The types of control codes you can specify depend on the device being accessed and the platform on which your application is running.</span></span> <span data-ttu-id="e3a6d-112">Приложения могут использовать стандартные управляющие коды или управляющие коды для конкретных устройств, чтобы выполнять прямые операции ввода-вывода на гибком диске, жестком диске, ленточном накопителе или устройстве чтения компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="e3a6d-112">Applications can use the standard control codes or device-specific control codes to perform direct input and output operations on a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3a6d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e3a6d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3a6d-114">Вызов DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="e3a6d-114">Calling DeviceIoControl</span></span>](calling-deviceiocontrol.md)
</dt> </dl>

 

 
