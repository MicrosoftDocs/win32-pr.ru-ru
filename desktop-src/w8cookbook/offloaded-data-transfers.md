---
title: Разгрузка передачи данных
description: Разгрузка передачи данных
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- Копировать разгрузку
- нагрузку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "105710393"
---
# <a name="offloaded-data-transfers"></a><span data-ttu-id="1f7c2-106">Разгрузка передачи данных</span><span class="sxs-lookup"><span data-stu-id="1f7c2-106">Offloaded data transfers</span></span>

## <a name="platforms"></a><span data-ttu-id="1f7c2-107">Платформы</span><span class="sxs-lookup"><span data-stu-id="1f7c2-107">Platforms</span></span>

<span data-ttu-id="1f7c2-108">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="1f7c2-108">**Clients** – Windows 8</span></span>  
<span data-ttu-id="1f7c2-109">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f7c2-109">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="1f7c2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1f7c2-110">Description</span></span>

<span data-ttu-id="1f7c2-111">Чтобы продвинуть перемещение данных хранилища, корпорация Майкрософт разработала новую технологию передачи данных — разгрузку передачи данных (ODX).</span><span class="sxs-lookup"><span data-stu-id="1f7c2-111">To advance the storage data movement, Microsoft has developed a new data transfer technology – offloaded data transfer (ODX).</span></span> <span data-ttu-id="1f7c2-112">Вместо использования буферизованных операций чтения и буферизованной записи Windows ODX запускает операцию копирования с разгрузкой Read и извлекает маркер, представляющий данные с устройства хранения, а затем использует разгрузку команды Write с маркером для запроса перемещения данных с исходного диска на целевой диск.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-112">Instead of using buffered read and buffered write operations, Windows ODX starts the copy operation with an offload read and retrieves a token representing the data from the storage device, then uses an offload write command with the token to request data movement from the source disk to the destination disk.</span></span> <span data-ttu-id="1f7c2-113">Диспетчер копирования запоминающих устройств выполняет перемещение данных в соответствии с маркером.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-113">The copy manager of the storage devices performs the data movement according to the token.</span></span> <span data-ttu-id="1f7c2-114">В Windows 8 ИТ-менеджер и администратор хранилища могут использовать функцию Windows ODX для взаимодействия с устройством хранения для перемещения больших файлов или данных через высокоскоростную сеть хранения.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-114">In the Windows 8, the IT manager and storage administrator are able to use the Windows ODX feature to interact with the storage device to move large files or data through the high-speed storage network.</span></span> <span data-ttu-id="1f7c2-115">Windows ODX значительно сокращает сетевой трафик клиента и использования времени ЦП во время передачи больших данных, так как все перемещения данных находятся в внутренней сети хранилища.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-115">Windows ODX will significantly reduce client-server network traffic and CPU time usage during large data transfers because all the data movement is at the backend storage network.</span></span> <span data-ttu-id="1f7c2-116">ODX можно использовать при развертывании виртуальных машин, массовом переносе данных и поддержке многоуровневого запоминающего устройства, а также снизить затраты на развертывание физического оборудования с помощью ODX и функций хранения с тонкой подготовкой.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-116">ODX can be used in virtual machine deployment, massive data migration, and tiered storage device support, and can lower the cost of physical hardware deployment through the ODX and thin provisioning storage features.</span></span>

> [!Note]  
> <span data-ttu-id="1f7c2-117">Эта функция будет работать только на устройствах хранения с реализацией спецификации SPC4 и SBC3.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-117">This feature will only work on storage devices with SPC4 and SBC3 specification implementation.</span></span>

 

## <a name="functional-details"></a><span data-ttu-id="1f7c2-118">Функциональные сведения</span><span class="sxs-lookup"><span data-stu-id="1f7c2-118">Functional details</span></span>

-   <span data-ttu-id="1f7c2-119">Функция Windows ODX встроена в подсистему копирования операционной системы Windows; во время перечисления хранилища Windows будет запрашивать возможность ODX устройства хранения.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-119">The Windows ODX feature is embedded in the copy engine of the Windows operating system; during storage enumeration, Windows will query the ODX capability of the storage device</span></span>
-   <span data-ttu-id="1f7c2-120">Копирование исходного устройства хранения и копирования целевого устройства хранения должно осуществляться в том же диспетчере копирования, что и для поддержки разгрузки копий</span><span class="sxs-lookup"><span data-stu-id="1f7c2-120">Copy source storage device and copy destination storage device should be managed under the same copy manager for copy offload support</span></span>
-   <span data-ttu-id="1f7c2-121">В случае сбоя операции разгрузки копирования диспетчер копирования устройства хранения должен вернуть соответствующие дополнительные данные для обработки ошибок приложений.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-121">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for the apps’ error handling</span></span>
-   <span data-ttu-id="1f7c2-122">При сбое операции разгрузки копирования Подсистема копирования Windows будет возвращаться к традиционной операции копирования.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-122">The Windows copy engine will fall back to the traditional copy operation if the copy offload operation fails</span></span>

## <a name="using-odx"></a><span data-ttu-id="1f7c2-123">Использование ODX</span><span class="sxs-lookup"><span data-stu-id="1f7c2-123">Using ODX</span></span>

-   <span data-ttu-id="1f7c2-124">Приложение для обмена данными должно гарантировать, что оба исходного LUN копируются и конечный LUN копирования ODX, прежде чем вызывать подпрограммы API ODX</span><span class="sxs-lookup"><span data-stu-id="1f7c2-124">The data transfer app must ensure both copy source LUN and copy destination LUN are ODX capable before calling the ODX API routines</span></span>
-   <span data-ttu-id="1f7c2-125">В проводнике Windows пользователи могут использовать "перетаскивание" или "копирование и вставка" для разгрузки копирования</span><span class="sxs-lookup"><span data-stu-id="1f7c2-125">In Windows explorer, users could use “drag” or “copy and paste” to perform copy offload</span></span>
-   <span data-ttu-id="1f7c2-126">Если исходный LUN и целевой LUN подключены к файловой системе, приложение должно вызвать только ФСКТЛ \_ разгрузки \_ Read и фсктл, \_ \_ чтобы выполнить перенос данных из ИСХОДНОГО LUN в целевой LUN.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-126">When the source LUN and destination LUN are mounted with the file system, the app must only call FSCTL\_Offload\_Read and FSCTL\_Offload\_Write to perform data transfer from the source LUN to the destination LUN</span></span>
-   <span data-ttu-id="1f7c2-127">В случае сбоя операции разгрузки копирования диспетчер копирования устройства хранения должен вернуть соответствующие дополнительные данные для обработки ошибок приложений.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-127">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for apps’ error handling</span></span>
-   <span data-ttu-id="1f7c2-128">Если исходный LUN или целевой LUN не подключен к файловой системе и заблокирован, приложение должно вызвать функцию "хранилище IOCTL" \_ \_ Управление \_ \_ \_ атрибутами набора данных с помощью девицедсмактион \_ оффлоадреад или девицедсмактион \_ оффлоадврите действие для выполнения разгрузки копирования.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-128">When the source LUN or destination LUN is not mounted with the file system and locked, the app must call IOCTL\_STORAGE\_MANAGE\_DATA\_SET\_ATTRIBUTES with DeviceDsmAction\_OffloadRead or DeviceDsmAction\_OffloadWrite action to perform copy offload</span></span>
-   <span data-ttu-id="1f7c2-129">Приложения для управления хранением данных могут использовать \_ \_ API-интерфейс Pass, чтобы выполнить разгрузку при передаче, если как исходный, так и конечный LUN не подключены к файловой системе и заблокированы</span><span class="sxs-lookup"><span data-stu-id="1f7c2-129">Storage management apps may use SCSI\_PASS\_THROUGH API to perform offloaded data transfers when both source and destination LUNs are not mounted with any file system and locked</span></span>

## <a name="tests"></a><span data-ttu-id="1f7c2-130">Тесты</span><span class="sxs-lookup"><span data-stu-id="1f7c2-130">Tests</span></span>

-   <span data-ttu-id="1f7c2-131">Чтобы обеспечить надежный пользовательский интерфейс, проверьте сертификацию Windows ODX массива хранения данных.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-131">To ensure a robust user experience, verify the Windows ODX certification of the storage array</span></span>
-   <span data-ttu-id="1f7c2-132">Устройство хранения должно соответствовать требованиям сертификации для передачи данных, разгрузкой которых является Windows (используется для логотипа) для поддержки функции ODX.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-132">The storage device must comply with Windows Offloaded Data Transfers certification (used to be Logo) requirements to support ODX feature</span></span>
-   <span data-ttu-id="1f7c2-133">С помощью комплекта сертификации оборудования для передачи данных Windows можно проверить поддержку функций ODX для устройств хранения.</span><span class="sxs-lookup"><span data-stu-id="1f7c2-133">Use the Windows Offloaded Data Transfers Hardware Certification Kit to verify the ODX feature support of the storage devices</span></span>

## <a name="resources"></a><span data-ttu-id="1f7c2-134">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="1f7c2-134">Resources</span></span>

-   <span data-ttu-id="1f7c2-135">T10 XCOPY Lite Spec (11-059r8)</span><span class="sxs-lookup"><span data-stu-id="1f7c2-135">T10 XCOPY Lite Spec (11-059r8)</span></span>
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [<span data-ttu-id="1f7c2-136">Службы панели мониторинга оборудования</span><span class="sxs-lookup"><span data-stu-id="1f7c2-136">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)
-   [<span data-ttu-id="1f7c2-137">\_Структура передачи \_ SCSI</span><span class="sxs-lookup"><span data-stu-id="1f7c2-137">SCSI\_PASS\_THROUGH Structure</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 