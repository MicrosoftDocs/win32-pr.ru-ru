---
description: Двоичные файлы Windows Server 2003 с пакетом обновления 1 (SP1) совместимы с Windows Vista и Windows Server 2008. Однако двоичные файлы из более ранних версий Windows должны быть перекомпилированы.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Перенос приложений резервного копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544970"
---
# <a name="porting-backup-applications"></a><span data-ttu-id="2f7a4-104">Перенос приложений резервного копирования</span><span class="sxs-lookup"><span data-stu-id="2f7a4-104">Porting Backup Applications</span></span>

<span data-ttu-id="2f7a4-105">Двоичные файлы Windows Server 2003 с пакетом обновления 1 (SP1) совместимы с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-105">Binaries from Windows Server 2003 with Service Pack 1 (SP1) are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="2f7a4-106">Однако двоичные файлы из более ранних версий Windows должны быть перекомпилированы.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-106">However, binaries from earlier versions of Windows must be recompiled.</span></span>

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a><span data-ttu-id="2f7a4-107">Перенос приложений Windows XP Backup на Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f7a4-107">Porting Windows XP Backup Applications to Windows Vista</span></span>

<span data-ttu-id="2f7a4-108">С момента выпуска Windows XP изменилось несколько интерфейсов VSS.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-108">Several VSS interfaces have changed since Windows XP.</span></span> <span data-ttu-id="2f7a4-109">Как минимум, приложения Windows XP должны быть перекомпилированы с помощью файлов заголовков и библиотек из пакета SDK для VSS 7,2 или пакета SDK для Windows Vista или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-109">At a minimum, Windows XP applications must be recompiled using header files and libraries from the VSS 7.2 SDK or the Windows Vista or Windows Server 2008 SDK.</span></span>

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a><span data-ttu-id="2f7a4-110">Перенос приложений резервного копирования Windows Server 2003 с пакетом обновления 1 (SP1) на Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f7a4-110">Porting Windows Server 2003 SP1 Backup Applications to Windows Vista</span></span>

<span data-ttu-id="2f7a4-111">Двоичные файлы Windows Server 2003 с пакетом обновления 1 (SP1) совместимы с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-111">Binaries from Windows Server 2003 with SP1 are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="2f7a4-112">Однако большинство приложений резервного копирования Windows Server 2003 с пакетом обновления 1 (SP1) необходимо обновить для учета новых функций, которые описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-112">However, most Windows Server 2003 with SP1 backup applications must be updated to account for new features, which are described in the following sections.</span></span>

## <a name="compiling-backup-applications-for-windows-vista"></a><span data-ttu-id="2f7a4-113">Компиляция приложений резервного копирования для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f7a4-113">Compiling Backup Applications for Windows Vista</span></span>

<span data-ttu-id="2f7a4-114">Приложения, использующие интерфейсы, доступные в Windows Server 2003, могут быть скомпилированы с помощью файлов заголовков и библиотек, предоставленных в пакете SDK для VSS 7,2.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-114">Applications that use interfaces available in Windows Server 2003 can be compiled using header files and libraries provided in the VSS 7.2 SDK.</span></span> <span data-ttu-id="2f7a4-115">Для использования новых интерфейсов приложения должны быть перекомпилированы с помощью файлов заголовков и библиотек, входящих в пакет SDK для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-115">To use new interfaces, applications must be recompiled using the header files and libraries included in the Windows Vista SDK.</span></span>

> [!Note]  
> <span data-ttu-id="2f7a4-116">Двоичные файлы, скомпилированные с помощью Windows Vista или Windows Server 2008, несовместимы с Windows Server 2003 с пакетом обновления 1 (SP1) или более ранними версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="2f7a4-116">Binaries compiled using Windows Vista or Windows Server 2008 are not compatible with Windows Server 2003 with SP1 or earlier versions of Windows.</span></span>

 

 

 



