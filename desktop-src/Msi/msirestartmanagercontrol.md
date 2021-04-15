---
description: Свойство МСИРЕСТАРТМАНАЖЕРКОНТРОЛ указывает, использует ли пакет установщик Windows функцию диалогового окна Диспетчер перезапуска или Филесинусе.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: МСИРЕСТАРТМАНАЖЕРКОНТРОЛ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669044"
---
# <a name="msirestartmanagercontrol-property"></a><span data-ttu-id="34f89-103">МСИРЕСТАРТМАНАЖЕРКОНТРОЛ, свойство</span><span class="sxs-lookup"><span data-stu-id="34f89-103">MSIRESTARTMANAGERCONTROL property</span></span>

<span data-ttu-id="34f89-104">Свойство **мсирестартманажерконтрол** указывает, использует ли пакет установщик Windows функцию [диалогового окна](filesinuse-dialog.md) [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) или филесинусе.</span><span class="sxs-lookup"><span data-stu-id="34f89-104">The **MSIRESTARTMANAGERCONTROL** Property specifies whether the Windows Installer package uses the [Restart Manager](../rstmgr/restart-manager-portal.md) or [FilesInUse Dialog](filesinuse-dialog.md) functionality.</span></span>

## <a name="value"></a><span data-ttu-id="34f89-105">Значение</span><span class="sxs-lookup"><span data-stu-id="34f89-105">Value</span></span>



| <span data-ttu-id="34f89-106">Значение</span><span class="sxs-lookup"><span data-stu-id="34f89-106">Value</span></span>                                                                                        | <span data-ttu-id="34f89-107">Значение</span><span class="sxs-lookup"><span data-stu-id="34f89-107">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34f89-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="34f89-108"><dt>0</dt></span></span> </dl>                 | <span data-ttu-id="34f89-109">Это значение по умолчанию, если свойство не задано.</span><span class="sxs-lookup"><span data-stu-id="34f89-109">This is the default value if the property is not set.</span></span> <span data-ttu-id="34f89-110">Установщик Windows всегда пытается использовать [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34f89-110">Windows Installer always attempts to use the [Restart Manager](../rstmgr/restart-manager-portal.md) on Windows Vista.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="34f89-111"><dt>Включен</dt></span><span class="sxs-lookup"><span data-stu-id="34f89-111"><dt>"Disable"</dt></span></span> </dl>         | <span data-ttu-id="34f89-112">Отключает взаимодействие пакета с [диспетчером перезапуска](../rstmgr/restart-manager-portal.md).</span><span class="sxs-lookup"><span data-stu-id="34f89-112">Disables interaction of the package with the [Restart Manager](../rstmgr/restart-manager-portal.md).</span></span> <span data-ttu-id="34f89-113">Установщик Windows использует [диалоговое окно филесинусе](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="34f89-113">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="34f89-114"><dt>"Дисаблешутдовн"</dt></span><span class="sxs-lookup"><span data-stu-id="34f89-114"><dt>"DisableShutdown"</dt></span></span> </dl> | <span data-ttu-id="34f89-115">Установщик Windows использует [диалоговое окно филесинусе](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="34f89-115">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="34f89-116">Этот параметр отключает попытки [диспетчера](../rstmgr/restart-manager-portal.md) перезапуска по устранению перезапусков при установке пакета установщик Windows, который не был создан для использования диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="34f89-116">This setting disables attempts by the [Restart Manager](../rstmgr/restart-manager-portal.md) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="34f89-117">Установщик по-прежнему использует диспетчер перезапуска для обнаружения файлов, используемых приложениями.</span><span class="sxs-lookup"><span data-stu-id="34f89-117">The installer still uses the Restart Manager to detect files in use by applications.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="34f89-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34f89-118">Remarks</span></span>

<span data-ttu-id="34f89-119">Свойство **мсирестартманажерконтрол** игнорируется, если [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) недоступен или отключен.</span><span class="sxs-lookup"><span data-stu-id="34f89-119">The **MSIRESTARTMANAGERCONTROL** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

<span data-ttu-id="34f89-120">Значение этого свойства можно изменить с помощью преобразований настройки или обновлений.</span><span class="sxs-lookup"><span data-stu-id="34f89-120">The value of this property can be modified using customization transforms or upgrades.</span></span> <span data-ttu-id="34f89-121">Изменение значения этого свойства с настраиваемых действий не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="34f89-121">Changing the value of this property from custom actions has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f89-122">Требования</span><span class="sxs-lookup"><span data-stu-id="34f89-122">Requirements</span></span>



| <span data-ttu-id="34f89-123">Требование</span><span class="sxs-lookup"><span data-stu-id="34f89-123">Requirement</span></span> | <span data-ttu-id="34f89-124">Значение</span><span class="sxs-lookup"><span data-stu-id="34f89-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34f89-125">Версия</span><span class="sxs-lookup"><span data-stu-id="34f89-125">Version</span></span><br/> | <span data-ttu-id="34f89-126">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34f89-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34f89-127">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34f89-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34f89-128">Сведения о минимальном пакете обновления, требуемом для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="34f89-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34f89-129">См. также</span><span class="sxs-lookup"><span data-stu-id="34f89-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f89-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="34f89-130">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="34f89-131">дисаблеаутоматикаппликатионшутдовн</span><span class="sxs-lookup"><span data-stu-id="34f89-131">DisableAutomaticApplicationShutdown</span></span>](disableautomaticapplicationshutdown.md)
</dt> <dt>

[<span data-ttu-id="34f89-132">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="34f89-132">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
