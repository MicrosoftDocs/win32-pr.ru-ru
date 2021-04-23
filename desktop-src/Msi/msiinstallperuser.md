---
description: Свойства МСИИНСТАЛЛПЕРУСЕР и ALLUSERS могут быть заданы пользователем во время установки, через пользовательский интерфейс или в командной строке, чтобы запросить, что установщик Windows установить пакет двойного назначения для текущего пользователя или всех пользователей компьютера.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: МСИИНСТАЛЛПЕРУСЕР, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651663"
---
# <a name="msiinstallperuser-property"></a><span data-ttu-id="e2ed9-103">МСИИНСТАЛЛПЕРУСЕР, свойство</span><span class="sxs-lookup"><span data-stu-id="e2ed9-103">MSIINSTALLPERUSER property</span></span>

<span data-ttu-id="e2ed9-104">Свойства **мсиинсталлперусер** и [**ALLUSERS**](allusers.md) могут быть заданы пользователем во время установки, через пользовательский интерфейс или в командной строке, чтобы запросить, что установщик Windows установить пакет двойного назначения для текущего пользователя или всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-104">The **MSIINSTALLPERUSER** and the [**ALLUSERS**](allusers.md) properties can be set by the user at installation time, through the user interface or on a command line, to request that the Windows Installer install a dual-purpose package for the current user or all users of the computer.</span></span> <span data-ttu-id="e2ed9-105">Чтобы использовать свойство **мсиинсталлперусер** , значение свойства [**ALLUSERS**](allusers.md) должно быть равно 2, а пакет должен быть создан, чтобы иметь возможность установки в контексте на пользователя или на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-105">To use the **MSIINSTALLPERUSER** property, the value of the [**ALLUSERS**](allusers.md) property must be 2 and the package has to have been authored to be capable of installation into either the per-user or a per-machine context.</span></span> <span data-ttu-id="e2ed9-106">Сведения о создании пакета для двойного назначения см. в разделе [Создание отдельного пакета](single-package-authoring.md).</span><span class="sxs-lookup"><span data-stu-id="e2ed9-106">For information about authoring a dual-purpose package, see [Single Package Authoring](single-package-authoring.md).</span></span> <span data-ttu-id="e2ed9-107">Если значение свойства **ALLUSERS** не равно 2, значение свойства **мсиинсталлперусер** игнорируется и не влияет на установку.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-107">If the value of the **ALLUSERS** property does not equal 2, the value of the **MSIINSTALLPERUSER** property is ignored and has no effect on the installation.</span></span> <span data-ttu-id="e2ed9-108">Значение свойства **мсиинсталлперусер** игнорируется при установке пакета с помощью установщик Windows 4,5 или более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-108">The value of **MSIINSTALLPERUSER** property is ignored when installing the package using Windows Installer 4.5 or earlier.</span></span>

<span data-ttu-id="e2ed9-109">Чтобы запросить, что установщик Windows установить пакет двойного назначения в [контексте установки](installation-context.md)на компьютере, пользователь может установить значение свойства **мсиинсталлперусер** в пустую строку (""), а значение свойства [**ALLUSERS**](allusers.md) — в 2 с помощью созданного пользовательского интерфейса или командной строки.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-109">To request that the Windows Installer install the dual-purpose package in the per-machine [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to an empty string ("") and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="e2ed9-110">Чтобы запросить, что установщик Windows установить пакет с двойным набором данных в [контексте установки](installation-context.md)на уровне пользователя, пользователь может присвоить свойству **мсиинсталлперусер** значение 1, а свойству [**ALLUSERS**](allusers.md) — значение 2 с помощью созданного пользовательского интерфейса или командной строки.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-110">To request that the Windows Installer install the dual-purpose package in the per-user [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to 1 and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="e2ed9-111">Если значение свойства [**ALLUSERS**](allusers.md) не равно 2, установщик Windows игнорирует значение свойства **мсиинсталлперусер** .</span><span class="sxs-lookup"><span data-stu-id="e2ed9-111">If the value of the [**ALLUSERS**](allusers.md) property does not equal 2, the Windows Installer ignores the value of the **MSIINSTALLPERUSER** property.</span></span> <span data-ttu-id="e2ed9-112">Если установщик Windows устанавливает приложение в контексте каждого компьютера, оно сбрасывает значение свойства **ALLUSERS** на 1.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-112">If Windows Installer installs the application in the per-machine context, it resets the value of the **ALLUSERS** property to 1.</span></span> <span data-ttu-id="e2ed9-113">Если установщик Windows устанавливает приложение в контексте для каждого пользователя, оно сбрасывает значение свойства **ALLUSERS** в пустую строку ("").</span><span class="sxs-lookup"><span data-stu-id="e2ed9-113">If Windows Installer installs the application in the per-user context, it resets the value of the **ALLUSERS** property to an empty string ("").</span></span> <span data-ttu-id="e2ed9-114">Таким образом, приложения, установленные для каждого пользователя, получают все обновления или исправления для каждого пользователя, а установленные на компьютере приложения получают обновления или исправления для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-114">Applications that have been installed per-user therefore receive all updates or repairs on a per-user basis and applications installed per-machine receive updates or repairs on a per-machine basis.</span></span>

<span data-ttu-id="e2ed9-115">**[Установщик Windows 4,5 или более ранней](not-supported-in-windows-installer-4-5.md)версии:** свойство **мсиинсталлперусер** игнорируется версиями, предшествующими установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-115">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** The **MSIINSTALLPERUSER** property is ignored by versions earlier than Windows Installer 5.0.</span></span>

## <a name="default-value"></a><span data-ttu-id="e2ed9-116">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2ed9-116">Default Value</span></span>

<span data-ttu-id="e2ed9-117">Рекомендуемый контекст установки по умолчанию — "на пользователя" для пакета с двумя целями.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-117">The recommended default installation context is per-user for a dual-purpose package.</span></span> <span data-ttu-id="e2ed9-118">Автор МСИИНСТАЛЛПЕРУСЕР = 1 и ALLUSERS = 2 в [таблице свойств](property-table.md) пакета с двойным набором значений, чтобы указать в качестве контекста установки по умолчанию для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-118">Author MSIINSTALLPERUSER=1 and ALLUSERS=2 in the [Property table](property-table.md) of the dual-purpose package to specify per-user as the default installation context.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ed9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2ed9-119">Remarks</span></span>

<span data-ttu-id="e2ed9-120">Можно убедиться, что свойство **мсиинсталлперусер** не было задано, задав его значение пустой строкой (""), мсиинсталлперусер = "".</span><span class="sxs-lookup"><span data-stu-id="e2ed9-120">You can ensure the **MSIINSTALLPERUSER** property has not been set by setting its value to an empty string (""), MSIINSTALLPERUSER="".</span></span>

<span data-ttu-id="e2ed9-121">Контекст установки определяет значения свойств [**DesktopFolder**](desktopfolder.md), [**программенуфолдер**](programmenufolder.md), [**programmenufolder**](startmenufolder.md), [**стартупфолдер**](startupfolder.md), [**темплатефолдер**](templatefolder.md), [**админтулсфолдер**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**коммонфилесфолдер**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)и [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="e2ed9-121">The installation context determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="e2ed9-122">Контекст установки определяет части реестра, в которых записи в [таблице реестра](registry-table.md) и [таблице ремоверегистри](removeregistry-table.md)с параметром-1 в корневом столбце, записываются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-122">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span> <span data-ttu-id="e2ed9-123">Дополнительные сведения о контексте установки см. в разделе [контекст установки](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="e2ed9-123">For information about the installation context, see [Installation Context](installation-context.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ed9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e2ed9-124">Requirements</span></span>



| <span data-ttu-id="e2ed9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e2ed9-125">Requirement</span></span> | <span data-ttu-id="e2ed9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e2ed9-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ed9-127">Версия</span><span class="sxs-lookup"><span data-stu-id="e2ed9-127">Version</span></span><br/> | <span data-ttu-id="e2ed9-128">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e2ed9-129">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e2ed9-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2ed9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e2ed9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ed9-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2ed9-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="e2ed9-132">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="e2ed9-132">**ALLUSERS**</span></span>](allusers.md)
</dt> <dt>

[<span data-ttu-id="e2ed9-133">Контекст установки</span><span class="sxs-lookup"><span data-stu-id="e2ed9-133">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="e2ed9-134">Создание отдельных пакетов</span><span class="sxs-lookup"><span data-stu-id="e2ed9-134">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




