---
description: Свойство МСИДИСАБЛЕРМРЕСТАРТ определяет, каким способом приложения или службы, использующие файлы, затрагиваемые обновлением, должны быть выключены и перезапущены, чтобы обеспечить установку обновления.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: МСИДИСАБЛЕРМРЕСТАРТ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652013"
---
# <a name="msidisablermrestart-property"></a><span data-ttu-id="55764-103">МСИДИСАБЛЕРМРЕСТАРТ, свойство</span><span class="sxs-lookup"><span data-stu-id="55764-103">MSIDISABLERMRESTART property</span></span>

<span data-ttu-id="55764-104">Свойство **мсидисаблермрестарт** определяет, каким способом приложения или службы, использующие файлы, затрагиваемые обновлением, должны быть выключены и перезапущены, чтобы обеспечить установку обновления.</span><span class="sxs-lookup"><span data-stu-id="55764-104">The **MSIDISABLERMRESTART** property determines how applications or services that are currently using files affected by an update should be shut down and restarted to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="55764-105">Значение</span><span class="sxs-lookup"><span data-stu-id="55764-105">Value</span></span>



| <span data-ttu-id="55764-106">Значение</span><span class="sxs-lookup"><span data-stu-id="55764-106">Value</span></span>                                                                        | <span data-ttu-id="55764-107">Значение</span><span class="sxs-lookup"><span data-stu-id="55764-107">Meaning</span></span>                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55764-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="55764-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="55764-109">Все системные службы, которые были отключены для установки обновления, перезапускаются.</span><span class="sxs-lookup"><span data-stu-id="55764-109">All system services that were shut down to install the update are restarted.</span></span> <span data-ttu-id="55764-110">Все приложения, зарегистрированные в [диспетчере перезапуска](../rstmgr/restart-manager-portal.md) , перезапускаются.</span><span class="sxs-lookup"><span data-stu-id="55764-110">All applications that registered themselves with the [Restart Manager](../rstmgr/restart-manager-portal.md) are restarted.</span></span><br/> |
| <dl> <span data-ttu-id="55764-111"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="55764-111"><dt>1</dt></span></span> </dl> | <span data-ttu-id="55764-112">Процессы, которые были закрыты с помощью [диспетчера перезапуска](../rstmgr/restart-manager-portal.md) во время установки обновления, не будут перезапущены после применения обновления.</span><span class="sxs-lookup"><span data-stu-id="55764-112">Processes that were shut down using the [Restart Manager](../rstmgr/restart-manager-portal.md) while installing the update will not be restarted after the update is applied.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="55764-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55764-113">Remarks</span></span>

<span data-ttu-id="55764-114">Свойство **мсидисаблермрестарт** игнорируется, если [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) недоступен или отключен.</span><span class="sxs-lookup"><span data-stu-id="55764-114">The **MSIDISABLERMRESTART** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="55764-115">Требования</span><span class="sxs-lookup"><span data-stu-id="55764-115">Requirements</span></span>



| <span data-ttu-id="55764-116">Требование</span><span class="sxs-lookup"><span data-stu-id="55764-116">Requirement</span></span> | <span data-ttu-id="55764-117">Значение</span><span class="sxs-lookup"><span data-stu-id="55764-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55764-118">Версия</span><span class="sxs-lookup"><span data-stu-id="55764-118">Version</span></span><br/> | <span data-ttu-id="55764-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="55764-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="55764-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="55764-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="55764-121">Сведения о минимальном пакете обновления, требуемом для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="55764-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55764-122">См. также</span><span class="sxs-lookup"><span data-stu-id="55764-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55764-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="55764-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="55764-124">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="55764-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
