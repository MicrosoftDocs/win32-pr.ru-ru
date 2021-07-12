---
description: Поставщики WMI безопасности можно использовать для сценариев WMI и для создания управляемого поставщика безопасности.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Поставщики WMI для системы безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d81833abff5160847678d094694702e4711de90
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581992"
---
# <a name="security-wmi-providers"></a><span data-ttu-id="6e434-103">Поставщики WMI для системы безопасности</span><span class="sxs-lookup"><span data-stu-id="6e434-103">Security WMI Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="6e434-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="6e434-104">Purpose</span></span>

<span data-ttu-id="6e434-105">поставщики WMI безопасности позволяют администраторам и программистам настраивать шифрование диска BitLocker (BDE) и доверенный платформенный модуль (TPM) (TPM) с помощью инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6e434-105">The Security WMI providers enable administrators and programmers to configure BitLocker Drive Encryption (BDE) and the Trusted Platform Module (TPM) using Windows Management Instrumentation (WMI).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6e434-106">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="6e434-106">Developer audience</span></span>

<span data-ttu-id="6e434-107">в этом документе указывается интерфейс поставщика WMI для управления и настройки шифрование диска BitLocker (BDE) и доверенный платформенный модуль (TPM) (TPM) на Windows server 2008 R2 и Windows Server 2008 для серверов, а также Windows 7 и Windows Vista для клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="6e434-107">This document specifies the WMI provider interface for managing and configuring BitLocker Drive Encryption (BDE) and Trusted Platform Module (TPM) on Windows Server 2008 R2 and Windows Server 2008 for servers, and Windows 7 and Windows Vista for client computers.</span></span> <span data-ttu-id="6e434-108">Он предназначен для чтения с помощью сценариев записи, элементов пользовательского интерфейса или других средств администрирования для BDE или TPM.</span><span class="sxs-lookup"><span data-stu-id="6e434-108">It is intended to be read by those writing scripts, user interface elements, or other administrative tools for BDE or the TPM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6e434-109">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="6e434-109">Run-time requirements</span></span>

<span data-ttu-id="6e434-110">Для поставщиков WMI безопасности требуется MOF-файл, указанный в каждом поставщике и поддерживаемой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="6e434-110">The Security WMI Providers require the .mof file specified with each provider and a supported operating system.</span></span> <span data-ttu-id="6e434-111">минимальная операционная система — либо Windows Server 2008, либо Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6e434-111">The minimum operating system is either Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6e434-112">шифрование диска BitLocker доступен только для версий Windows vista Enterprise и Windows vista Ultimate Windows vista.</span><span class="sxs-lookup"><span data-stu-id="6e434-112">BitLocker Drive Encryption is only available for the Windows Vista Enterprise and Windows Vista Ultimate versions of Windows Vista.</span></span> <span data-ttu-id="6e434-113">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="6e434-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6e434-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="6e434-114">In this section</span></span>



| <span data-ttu-id="6e434-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="6e434-115">Topic</span></span>                                                                               | <span data-ttu-id="6e434-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6e434-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="6e434-117">Сведения о поставщиках WMI для системы безопасности</span><span class="sxs-lookup"><span data-stu-id="6e434-117">About Security WMI Providers</span></span>](about-security-wmi-providers.md)<br/>         | <span data-ttu-id="6e434-118">Краткий обзор поставщиков WMI для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6e434-118">Brief overview of the Security WMI Providers.</span></span><br/>           |
| [<span data-ttu-id="6e434-119">Справочник по поставщикам WMI для системы безопасности</span><span class="sxs-lookup"><span data-stu-id="6e434-119">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md)<br/> | <span data-ttu-id="6e434-120">Справочная документация по поставщикам WMI безопасности.</span><span class="sxs-lookup"><span data-stu-id="6e434-120">Reference documentation for the Security WMI Providers.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="6e434-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6e434-121">Additional resources</span></span>

<span data-ttu-id="6e434-122">Ниже приведены дополнительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6e434-122">The following are additional resources.</span></span>



| <span data-ttu-id="6e434-123">Ресурс</span><span class="sxs-lookup"><span data-stu-id="6e434-123">Resource</span></span>     | <span data-ttu-id="6e434-124">Описание</span><span class="sxs-lookup"><span data-stu-id="6e434-124">Description</span></span>                                                                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e434-125">Классы</span><span class="sxs-lookup"><span data-stu-id="6e434-125">Classes</span></span>      | <span data-ttu-id="6e434-126">Дополнительные сведения о поставщиках WMI безопасности см. в разделе [**Win32 \_ Енкриптаблеволуме**](win32-encryptablevolume.md) и [**Win32 \_ TPM**](win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="6e434-126">For more information about the Security WMI providers, see [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md).</span></span> |



 

 

 




