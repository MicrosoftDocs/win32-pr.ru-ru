---
description: Свойство МСИРМШУТДОВН определяет, как приложения или службы, использующие файлы, затрагиваемые обновлением, должны завершить работу, чтобы включить установку обновления.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: МСИРМШУТДОВН, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669042"
---
# <a name="msirmshutdown-property"></a><span data-ttu-id="4983e-103">МСИРМШУТДОВН, свойство</span><span class="sxs-lookup"><span data-stu-id="4983e-103">MSIRMSHUTDOWN property</span></span>

<span data-ttu-id="4983e-104">Свойство **мсирмшутдовн** определяет, как приложения или службы, использующие файлы, затрагиваемые обновлением, должны завершить работу, чтобы включить установку обновления.</span><span class="sxs-lookup"><span data-stu-id="4983e-104">The **MSIRMSHUTDOWN** property determines how applications or services that are currently using files affected by an update should be shut down to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="4983e-105">Значение</span><span class="sxs-lookup"><span data-stu-id="4983e-105">Value</span></span>



| <span data-ttu-id="4983e-106">Значение</span><span class="sxs-lookup"><span data-stu-id="4983e-106">Value</span></span>                                                                        | <span data-ttu-id="4983e-107">Значение</span><span class="sxs-lookup"><span data-stu-id="4983e-107">Meaning</span></span>                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4983e-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4983e-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4983e-109">Процессы или службы, которые сейчас используют файлы, затронутые обновлением, завершаются.</span><span class="sxs-lookup"><span data-stu-id="4983e-109">Processes or services that are currently using files affected by the update are shut down.</span></span><br/>                                                                                                                                                                   |
| <dl> <span data-ttu-id="4983e-110"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4983e-110"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4983e-111">Процессы или службы, которые сейчас используют файлы, затронутые обновлением, и которые не отвечают на [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md), принудительно завершают работу.</span><span class="sxs-lookup"><span data-stu-id="4983e-111">Processes or services that are currently using files affected by the update, and that do not respond to the [Restart Manager](../rstmgr/restart-manager-portal.md), are forced to shut down.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="4983e-112"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4983e-112"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4983e-113">Процессы или службы, которые используют файлы, затронутые обновлением, завершаются только в том случае, если они были зарегистрированы для перезапуска.</span><span class="sxs-lookup"><span data-stu-id="4983e-113">Processes or services that are currently using files affected by the update are shut down only if they have all been registered for a restart.</span></span> <span data-ttu-id="4983e-114">Если какой-либо процесс или служба не были зарегистрированы для перезапуска, то никакие процессы или службы не будут закрыты.</span><span class="sxs-lookup"><span data-stu-id="4983e-114">If any process or service has not been registered for a restart, then no processes or services are shut down.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4983e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4983e-115">Remarks</span></span>

<span data-ttu-id="4983e-116">Свойство **мсирмшутдовн** игнорируется, если [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) недоступен или отключен.</span><span class="sxs-lookup"><span data-stu-id="4983e-116">The **MSIRMSHUTDOWN** property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="4983e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4983e-117">Requirements</span></span>



| <span data-ttu-id="4983e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4983e-118">Requirement</span></span> | <span data-ttu-id="4983e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4983e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4983e-120">Версия</span><span class="sxs-lookup"><span data-stu-id="4983e-120">Version</span></span><br/> | <span data-ttu-id="4983e-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4983e-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4983e-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4983e-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4983e-123">Сведения о минимальном пакете обновления, требуемом для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4983e-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4983e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4983e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4983e-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="4983e-125">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="4983e-126">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="4983e-126">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
