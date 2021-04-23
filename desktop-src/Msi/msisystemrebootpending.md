---
description: Установщик устанавливает значение свойства Мсисистемребутпендинг равным 1, если имеется операция, ожидающая переименования файла.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Мсисистемребутпендинг, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675948"
---
# <a name="msisystemrebootpending-property"></a><span data-ttu-id="c19ac-103">Мсисистемребутпендинг, свойство</span><span class="sxs-lookup"><span data-stu-id="c19ac-103">MsiSystemRebootPending property</span></span>

<span data-ttu-id="c19ac-104">Установщик устанавливает значение свойства **мсисистемребутпендинг** равным 1, если имеется операция, ожидающая переименования файла.</span><span class="sxs-lookup"><span data-stu-id="c19ac-104">The installer sets the value of the **MsiSystemRebootPending** property to 1 if there is an operation pending to rename a file.</span></span>

<span data-ttu-id="c19ac-105">Авторы пакетов могут основывать условие в [таблице лаунчкондитион](launchcondition-table.md) этого свойства, чтобы предотвратить установку пакета в случаях, когда имеется операция, ожидающая переименования файла.</span><span class="sxs-lookup"><span data-stu-id="c19ac-105">Package authors can base a condition in the [LaunchCondition table](launchcondition-table.md) on this property to prevent the installation of their package in cases where there is an operation pending to rename a file.</span></span> <span data-ttu-id="c19ac-106">Это может быть сделано для предотвращения перезапуска операционной системы из-за переименования файла.</span><span class="sxs-lookup"><span data-stu-id="c19ac-106">This may be done to prevent a restart of the operating system caused by the renaming of the file.</span></span> <span data-ttu-id="c19ac-107">Установщик не устанавливает свойство **мсисистемребутпендинг** во всех случаях, требующих перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="c19ac-107">The installer does not set the **MsiSystemRebootPending** property in all cases that require a restart of the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="c19ac-108">Требования</span><span class="sxs-lookup"><span data-stu-id="c19ac-108">Requirements</span></span>



| <span data-ttu-id="c19ac-109">Требование</span><span class="sxs-lookup"><span data-stu-id="c19ac-109">Requirement</span></span> | <span data-ttu-id="c19ac-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c19ac-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c19ac-111">Версия</span><span class="sxs-lookup"><span data-stu-id="c19ac-111">Version</span></span><br/> | <span data-ttu-id="c19ac-112">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c19ac-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c19ac-113">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c19ac-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c19ac-114">Установщик Windows 4,5 в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c19ac-114">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c19ac-115">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c19ac-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c19ac-116">См. также</span><span class="sxs-lookup"><span data-stu-id="c19ac-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c19ac-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="c19ac-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c19ac-118">Перезагрузка системы</span><span class="sxs-lookup"><span data-stu-id="c19ac-118">System Reboots</span></span>](system-reboots.md)
</dt> <dt>

[<span data-ttu-id="c19ac-119">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="c19ac-119">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




