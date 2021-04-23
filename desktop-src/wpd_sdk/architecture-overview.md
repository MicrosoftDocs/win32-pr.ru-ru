---
description: Общие сведения об архитектуре
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Общие сведения об архитектуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912888"
---
# <a name="architecture-overview"></a><span data-ttu-id="7ab24-103">Общие сведения об архитектуре</span><span class="sxs-lookup"><span data-stu-id="7ab24-103">Architecture Overview</span></span>

<span data-ttu-id="7ab24-104">Архитектура WPD может быть разделена на три процесса.</span><span class="sxs-lookup"><span data-stu-id="7ab24-104">The WPD architecture can be divided into three processes.</span></span> <span data-ttu-id="7ab24-105">В этих процессах используются три основных компонента WPD: API, сериализатор и драйвер.</span><span class="sxs-lookup"><span data-stu-id="7ab24-105">Within these processes are the three primary components of WPD: the API, the serializer, and the driver.</span></span> <span data-ttu-id="7ab24-106">На следующем рисунке показаны процессы и компоненты, составляющие архитектуру WPD.</span><span class="sxs-lookup"><span data-stu-id="7ab24-106">The following illustration depicts the processes and components that constitute the WPD architecture.</span></span>

![Иллюстрация, демонстрирующая компоненты API, сериализатора и драйверов для WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a><span data-ttu-id="7ab24-108">Прикладной программный интерфейс WPD</span><span class="sxs-lookup"><span data-stu-id="7ab24-108">The WPD Application Programming Interface</span></span>

<span data-ttu-id="7ab24-109">API-интерфейс WPD реализован как внутрипроцессный сервер COM.</span><span class="sxs-lookup"><span data-stu-id="7ab24-109">The WPD API is implemented as an in-proc COM server.</span></span> <span data-ttu-id="7ab24-110">API использует стандартные API-интерфейсы Microsoft Win32 для связи с соответствующим драйвером WPD.</span><span class="sxs-lookup"><span data-stu-id="7ab24-110">The API uses standard Microsoft Win32 APIs to communicate with the appropriate WPD driver.</span></span> <span data-ttu-id="7ab24-111">Компонент, именуемый сериализатором WPD, используется как объектами API, так и драйвером для упаковки или распаковки параметров в буферах драйверов (UMDF) Windows Driver Foundation (ВДФ) или из них.</span><span class="sxs-lookup"><span data-stu-id="7ab24-111">A component called the WPD serializer is used by both API objects and the driver to pack or unpack parameters to or from Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) buffers.</span></span>

## <a name="the-wpd-serializer"></a><span data-ttu-id="7ab24-112">Сериализатор WPD</span><span class="sxs-lookup"><span data-stu-id="7ab24-112">The WPD Serializer</span></span>

<span data-ttu-id="7ab24-113">Сериализатор WPD реализован как внутрипроцессный COM-сервер.</span><span class="sxs-lookup"><span data-stu-id="7ab24-113">The WPD serializer is implemented as an in-proc COM server.</span></span> <span data-ttu-id="7ab24-114">API-интерфейс WPD использует сериализатор для упаковки команд и параметров в буферы сообщений, отправляемые драйверу.</span><span class="sxs-lookup"><span data-stu-id="7ab24-114">The WPD API uses the serializer to pack commands and parameters into message buffers that are sent to the driver.</span></span> <span data-ttu-id="7ab24-115">Драйвер использует сериализатор для распаковки этих буферов сообщений для обработки.</span><span class="sxs-lookup"><span data-stu-id="7ab24-115">The driver uses the serializer to unpack these message buffers for processing.</span></span> <span data-ttu-id="7ab24-116">Драйвер также использует сериализатор для упаковки данных и параметров в буферы ответов, возвращаемые в API-интерфейс WPD, а API-интерфейс WPD использует сериализатор для распаковки этих буферов ответа, чтобы вернуться к вызывающим объектам.</span><span class="sxs-lookup"><span data-stu-id="7ab24-116">The driver also uses the serializer to pack data and parameters into response buffers that are returned to the WPD API, and the WPD API uses the serializer to unpack these response buffers to return to callers.</span></span>

## <a name="wpd-driver"></a><span data-ttu-id="7ab24-117">Драйвер WPD</span><span class="sxs-lookup"><span data-stu-id="7ab24-117">WPD Driver</span></span>

<span data-ttu-id="7ab24-118">Драйвер WPD реализован как стандартный драйвер платформы драйверов (UMDF) Windows Driver Foundation (ВДФ).</span><span class="sxs-lookup"><span data-stu-id="7ab24-118">The WPD driver is implemented as a standard Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) driver.</span></span> <span data-ttu-id="7ab24-119">Драйверы WPD размещаются с помощью UMDF в отдельном процессе, называемом узлом драйверов.</span><span class="sxs-lookup"><span data-stu-id="7ab24-119">WPD drivers are hosted by UMDF in a separate process called the Driver Host.</span></span>

<span data-ttu-id="7ab24-120">Драйвер получает сообщения от отражателя UMDF (это не показано на схеме, так как получение буферов не имеет значения для драйвера.</span><span class="sxs-lookup"><span data-stu-id="7ab24-120">The driver receives messages from the UMDF reflector (this is not shown in the diagram, since how the buffers are received is not important to the driver.</span></span> <span data-ttu-id="7ab24-121">Дополнительные сведения см. в документации по UMDF.</span><span class="sxs-lookup"><span data-stu-id="7ab24-121">See UMDF documentation for more information).</span></span> <span data-ttu-id="7ab24-122">Драйвер реализует обработчик управляющего кода ввода-вывода (ИОКЛ), специфический для WPD, для обработки сообщений WPD, полученных API-интерфейсом WPD.</span><span class="sxs-lookup"><span data-stu-id="7ab24-122">The driver implements a WPD-specific I/O Control code (IOCL) handler to process WPD messages received by the WPD API.</span></span> <span data-ttu-id="7ab24-123">Драйвер использует сериализатор WPD для распаковки команд и параметров из этих буферов сообщений и для упаковки ответа в буфер возврата.</span><span class="sxs-lookup"><span data-stu-id="7ab24-123">The driver uses the WPD serializer to unpack commands and parameters from these message buffers, and to pack the response into the return buffer.</span></span>

<span data-ttu-id="7ab24-124">Драйверы WPD могут взаимодействовать с устройствами посредством драйвера режима ядра, обычно доступ к которым осуществляется с помощью файловых операций Win32 (CreateFile, ReadFile, WriteFile и т. д.).</span><span class="sxs-lookup"><span data-stu-id="7ab24-124">WPD drivers may communicate with their devices by going through a kernel-mode driver, typically accessed via Win32 file operations (that is, CreateFile, ReadFile, WriteFile, and so on).</span></span> <span data-ttu-id="7ab24-125">Для общих шин Корпорация Майкрософт предоставит стандартные драйверы ядра для поставщиков, которые позволят поставщикам поставлять решение драйверов только для пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="7ab24-125">For the common buses, Microsoft will provide standard kernel drivers for vendors to use, which will allow vendors to ship a user-mode-only driver solution.</span></span> <span data-ttu-id="7ab24-126">Кроме того, для устройств с устройствами (MSC) и классами запоминающих носителей Майкрософт предоставит драйверы классов WPD.</span><span class="sxs-lookup"><span data-stu-id="7ab24-126">In addition, for Media Transfer Protocol (MTP) and Mass Storage Class (MSC) devices, Microsoft will provide WPD class drivers.</span></span>

<span data-ttu-id="7ab24-127">Дополнительные сведения о драйверах WPD см. в документации по драйверу для переносных устройств Windows в комплекте драйверов для Windows.</span><span class="sxs-lookup"><span data-stu-id="7ab24-127">For more information about WPD drivers, see the Windows Portable Devices Driver documentation in the Windows Driver Kit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ab24-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7ab24-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ab24-129">**Общие сведения о приложении**</span><span class="sxs-lookup"><span data-stu-id="7ab24-129">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



