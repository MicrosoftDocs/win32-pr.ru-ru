---
description: Свойство ЕКСЕКУТЕМОДЕ указывает, как установщик выполняет обновления системы.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: ЕКСЕКУТЕМОДЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689516"
---
# <a name="executemode-property"></a><span data-ttu-id="6214a-103">ЕКСЕКУТЕМОДЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="6214a-103">EXECUTEMODE property</span></span>

<span data-ttu-id="6214a-104">Свойство **ексекутемоде** указывает, как установщик выполняет обновления системы.</span><span class="sxs-lookup"><span data-stu-id="6214a-104">The **EXECUTEMODE** property specifies how the installer executes system updates.</span></span> <span data-ttu-id="6214a-105">Это свойство может быть полезно, если необходимо запустить установку без фактического изменения системы.</span><span class="sxs-lookup"><span data-stu-id="6214a-105">This property may be useful when it is necessary to run an installation without actually changing the system.</span></span> <span data-ttu-id="6214a-106">Свойству можно присвоить значение None, чтобы отключить операции обновления, такие как установка файлов и значений реестра.</span><span class="sxs-lookup"><span data-stu-id="6214a-106">The property can be set to None to disable updating operations such as the installation of files and registry values.</span></span>

<span data-ttu-id="6214a-107">Это свойство может иметь одно из следующих двух значений.</span><span class="sxs-lookup"><span data-stu-id="6214a-107">This property can have one of the following two values.</span></span> <span data-ttu-id="6214a-108">Установщик проверяет только первую букву значения и не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6214a-108">The installer only examines the first letter of the value and is case insensitive.</span></span>

<dl> <dt>

<span data-ttu-id="6214a-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span><span class="sxs-lookup"><span data-stu-id="6214a-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span>
</dt> <dd>

<span data-ttu-id="6214a-110">В систему не вносятся изменения.</span><span class="sxs-lookup"><span data-stu-id="6214a-110">No changes are made to the system.</span></span> <span data-ttu-id="6214a-111">Установщик запускает пользовательский интерфейс, а затем запрашивает базу данных.</span><span class="sxs-lookup"><span data-stu-id="6214a-111">The installer runs the user interface and then queries the database.</span></span>

</dd> <dt>

<span data-ttu-id="6214a-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Индекса</span><span class="sxs-lookup"><span data-stu-id="6214a-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script</span></span>
</dt> <dd>

<span data-ttu-id="6214a-113">Все изменения в системе выполняются с помощью выполнения скриптов.</span><span class="sxs-lookup"><span data-stu-id="6214a-113">All changes to the system are made through script execution.</span></span> <span data-ttu-id="6214a-114">Это режим по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6214a-114">This is the default mode.</span></span>

</dd> </dl>

## <a name="default-value"></a><span data-ttu-id="6214a-115">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6214a-115">Default Value</span></span>

<span data-ttu-id="6214a-116">Если это свойство не определено, режим выполнения по умолчанию имеет значение script.</span><span class="sxs-lookup"><span data-stu-id="6214a-116">If this property is not defined, the execution mode defaults to Script.</span></span>

## <a name="requirements"></a><span data-ttu-id="6214a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6214a-117">Requirements</span></span>



| <span data-ttu-id="6214a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6214a-118">Requirement</span></span> | <span data-ttu-id="6214a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6214a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6214a-120">Версия</span><span class="sxs-lookup"><span data-stu-id="6214a-120">Version</span></span><br/> | <span data-ttu-id="6214a-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6214a-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6214a-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6214a-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6214a-123">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6214a-123">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6214a-124">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6214a-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6214a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6214a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6214a-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="6214a-126">Properties</span></span>](properties.md)
</dt> </dl>

 

 




