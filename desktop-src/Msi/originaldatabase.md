---
description: Установщик Windows задает для свойства Оригиналдатабасе путь к базе данных установки, используемой для запуска установки.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Оригиналдатабасе, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675431"
---
# <a name="originaldatabase-property"></a><span data-ttu-id="c6ec3-103">Оригиналдатабасе, свойство</span><span class="sxs-lookup"><span data-stu-id="c6ec3-103">OriginalDatabase property</span></span>

<span data-ttu-id="c6ec3-104">Установщик Windows задает для свойства **оригиналдатабасе** путь к базе данных установки, используемой для запуска установки.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-104">The Windows Installer sets the **OriginalDatabase** property to the path of the installation database used to launch the installation.</span></span> <span data-ttu-id="c6ec3-105">Если установка запускается из командной строки, это значение зависит от того, есть ли в свойстве [**REINSTALLMODE**](reinstallmode.md) параметр пакета повторного кэширования (флаг-v).</span><span class="sxs-lookup"><span data-stu-id="c6ec3-105">If the installation is launched from a command line, the value depends on whether the recache package option (the -v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>



| <span data-ttu-id="c6ec3-106">Метод установки</span><span class="sxs-lookup"><span data-stu-id="c6ec3-106">Installation Method</span></span>                                                                                                                                                                                  | <span data-ttu-id="c6ec3-107">Значение Оригиналдатабасе</span><span class="sxs-lookup"><span data-stu-id="c6ec3-107">OriginalDatabase Value</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="c6ec3-108">Любая установка, запущенная путем вызова пути к установочному пакету (MSI-файл).</span><span class="sxs-lookup"><span data-stu-id="c6ec3-108">Any installation launched by invoking the path of the installation package (.msi file).</span></span>                                                                                                              | <span data-ttu-id="c6ec3-109">Путь к установочному пакету (MSI-файлу).</span><span class="sxs-lookup"><span data-stu-id="c6ec3-109">Path to the installation package (.msi file).</span></span> |
| <span data-ttu-id="c6ec3-110">Установка, запущенная из командной строки.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-110">Installation launched from a command line.</span></span> <span data-ttu-id="c6ec3-111">Установка не запускается из пути пакета.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-111">The installation is not launched from a package path.</span></span> <span data-ttu-id="c6ec3-112">Параметр повторного кэширования (флаг-v) имеется в свойстве [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="c6ec3-112">The recache option (-v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>     | <span data-ttu-id="c6ec3-113">Путь к базе данных в источнике.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-113">Path to the database on the source.</span></span>           |
| <span data-ttu-id="c6ec3-114">Установка, запущенная из командной строки.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-114">Installation launched from a command line.</span></span> <span data-ttu-id="c6ec3-115">Установка не запускается из пути пакета.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-115">The installation is not launched from a package path.</span></span> <span data-ttu-id="c6ec3-116">Параметр повторного кэширования (флаг-v) отсутствует в свойстве [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="c6ec3-116">The recache option (-v flag) is not present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> | <span data-ttu-id="c6ec3-117">Путь к кэшированной базе данных.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-117">Path to the cached database.</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="c6ec3-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6ec3-118">Remarks</span></span>

<span data-ttu-id="c6ec3-119">Во время первой установки пользовательское действие, выполняемое перед [действием ресолвесаурце](resolvesource-action.md) , может использовать свойство **оригиналдатабасе** для определения расположения источника установки.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-119">During a first time installation, a custom action sequenced before the [ResolveSource action](resolvesource-action.md) can use the **OriginalDatabase** property to determine the location of the installation source.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ec3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c6ec3-120">Requirements</span></span>



| <span data-ttu-id="c6ec3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c6ec3-121">Requirement</span></span> | <span data-ttu-id="c6ec3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c6ec3-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ec3-123">Версия</span><span class="sxs-lookup"><span data-stu-id="c6ec3-123">Version</span></span><br/> | <span data-ttu-id="c6ec3-124">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c6ec3-125">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c6ec3-126">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6ec3-126">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c6ec3-127">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c6ec3-127">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6ec3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c6ec3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ec3-129">Свойства</span><span class="sxs-lookup"><span data-stu-id="c6ec3-129">Properties</span></span>](properties.md)
</dt> </dl>

 

 




