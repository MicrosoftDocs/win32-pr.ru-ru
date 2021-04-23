---
title: Глоссарий доступа к устройствам
description: Ниже приведены термины, используемые во всей документации по API доступа к устройствам.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412461"
---
# <a name="device-access-glossary"></a><span data-ttu-id="c4086-103">Глоссарий доступа к устройствам</span><span class="sxs-lookup"><span data-stu-id="c4086-103">Device Access Glossary</span></span>

<span data-ttu-id="c4086-104">Ниже приведены термины, используемые во всей документации по API доступа к устройствам.</span><span class="sxs-lookup"><span data-stu-id="c4086-104">The following are terms used throughout the documentation for the Device Access API.</span></span>

<dl> <dt>

<span data-ttu-id="c4086-105">**AppContainer**</span><span class="sxs-lookup"><span data-stu-id="c4086-105">**AppContainer**</span></span>
</dt> <dd>

<span data-ttu-id="c4086-106">Среда выполнения с высокой степенью ограничений, в которой выполняется процесс с ограниченным подмножеством привилегий пользователя.</span><span class="sxs-lookup"><span data-stu-id="c4086-106">A highly restricted execution environment in which a process runs with a reduced subset of the user's privileges.</span></span> <span data-ttu-id="c4086-107">Процесс, выполняющийся в AppContainer, называется процессом AppContainer.</span><span class="sxs-lookup"><span data-stu-id="c4086-107">A process that's running within an AppContainer is called an AppContainer process.</span></span> <span data-ttu-id="c4086-108">Процесс AppContainer изолирован от других процессов AppContainer и из профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="c4086-108">An AppContainer process is isolated from other AppContainer processes and from the user's profile.</span></span> <span data-ttu-id="c4086-109">Он имеет ограниченный доступ к очень небольшому подмножеству системных ресурсов, таких как файлы, устройства, разделы реестра, конечные точки вызова процедур (IPC)/ремоте (RPC) и сетевые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="c4086-109">It has limited access to a very small subset of system resources like files, devices, registry keys, interprocess communication (IPC)/remote procedure call (RPC) endpoints, and network resources.</span></span>

</dd> <dt>

<span data-ttu-id="c4086-110">**Привязка**</span><span class="sxs-lookup"><span data-stu-id="c4086-110">**Binding**</span></span>
</dt> <dd>

<span data-ttu-id="c4086-111">Связывание объекта доступа к устройству с определенным интерфейсом устройства.</span><span class="sxs-lookup"><span data-stu-id="c4086-111">Associating a device access object with a particular device interface.</span></span> <span data-ttu-id="c4086-112">Если привязка прошла успешно, приложения Магазина Windows могут использовать объект доступа к устройству в качестве брокера для взаимодействия с драйвером устройства.</span><span class="sxs-lookup"><span data-stu-id="c4086-112">If binding is successful, Windows Store apps can use the device access object as a broker to communicate with the device driver.</span></span>

</dd> <dt>

<span data-ttu-id="c4086-113">**Broker**</span><span class="sxs-lookup"><span data-stu-id="c4086-113">**Broker**</span></span>
</dt> <dd>

<span data-ttu-id="c4086-114">Компонент, предоставляющий доступ к ресурсу, который не предоставляется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c4086-114">A component that provides access to a resource that isn't granted by default.</span></span>

</dd> <dt>

<span data-ttu-id="c4086-115">**Привилегированное приложение**</span><span class="sxs-lookup"><span data-stu-id="c4086-115">**Privileged App**</span></span>
</dt> <dd>

<span data-ttu-id="c4086-116">Приложение, определенное в метаданных конкретного устройства, связанное с этим устройством, чтобы оно может взаимодействовать с ограниченным интерфейсом драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="c4086-116">An app that's identified in a particular device's metadata as associated with that device, so that it can communicate with the device driver's restricted interface.</span></span> <span data-ttu-id="c4086-117">Примером такого приложения может быть собственное приложение для воспроизведения музыки, которое имеет исключительные разрешения на синхронизацию с портативным музыкальным проигрывателем, когда приложения от конкурентов не могут.</span><span class="sxs-lookup"><span data-stu-id="c4086-117">An example of such an app might be a proprietary music playback app that has exclusive permission to sync with a portable music player, when apps from competitors can't.</span></span> <span data-ttu-id="c4086-118">Дополнительные сведения о настройке метаданных устройства или о том, как ограничить драйвер для привилегированных приложений, см. в статье [приложения устройства UWP для внутренних устройств](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span><span class="sxs-lookup"><span data-stu-id="c4086-118">For more information about how to set a device's metadata or how to restrict a driver to privileged apps, see [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span></span>

</dd> </dl>
