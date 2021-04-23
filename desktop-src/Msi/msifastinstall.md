---
description: Свойство МСИФАСТИНСТАЛЛ можно использовать для сокращения времени, необходимого для установки большого пакета установщик Windows.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: МСИФАСТИНСТАЛЛ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651979"
---
# <a name="msifastinstall-property"></a><span data-ttu-id="18094-103">МСИФАСТИНСТАЛЛ, свойство</span><span class="sxs-lookup"><span data-stu-id="18094-103">MSIFASTINSTALL property</span></span>

<span data-ttu-id="18094-104">Свойство **мсифастинсталл** можно использовать для сокращения времени, необходимого для установки большого пакета установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="18094-104">The **MSIFASTINSTALL** property can be used to reduce the time required to install a large Windows Installer package.</span></span> <span data-ttu-id="18094-105">Свойство может быть задано в командной строке или в таблице [свойств](property-table.md) для настройки операций, определяемых пользователем или разработчиком, которые не являются обязательными для установки.</span><span class="sxs-lookup"><span data-stu-id="18094-105">The property can be set on the command line or in the [Property](property-table.md) table to configure operations that the user or developer determines are non-essential for the installation.</span></span>

<span data-ttu-id="18094-106">Значение свойства **мсифастинсталл** может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="18094-106">The value of the **MSIFASTINSTALL** property can be a combination of the following values.</span></span>



| <span data-ttu-id="18094-107">Значение</span><span class="sxs-lookup"><span data-stu-id="18094-107">Value</span></span> | <span data-ttu-id="18094-108">Значение</span><span class="sxs-lookup"><span data-stu-id="18094-108">Meaning</span></span>                                                                      |
|-------|------------------------------------------------------------------------------|
| <span data-ttu-id="18094-109">0</span><span class="sxs-lookup"><span data-stu-id="18094-109">0</span></span>     | <span data-ttu-id="18094-110">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="18094-110">Default value</span></span>                                                                |
| <span data-ttu-id="18094-111">1</span><span class="sxs-lookup"><span data-stu-id="18094-111">1</span></span>     | <span data-ttu-id="18094-112">Для этой установки нет сохраненных точек восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="18094-112">No system restore point is saved for this installation.</span></span>                      |
| <span data-ttu-id="18094-113">2</span><span class="sxs-lookup"><span data-stu-id="18094-113">2</span></span>     | <span data-ttu-id="18094-114">Выполнять только [Расчет стоимости файлов](file-costing.md) и пропустить проверку других затрат.</span><span class="sxs-lookup"><span data-stu-id="18094-114">Perform only [File Costing](file-costing.md) and skip checking other costs.</span></span> |
| <span data-ttu-id="18094-115">4</span><span class="sxs-lookup"><span data-stu-id="18094-115">4</span></span>     | <span data-ttu-id="18094-116">Сократите частоту сообщений о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="18094-116">Reduce the frequency of progress messages.</span></span>                                   |



 

<span data-ttu-id="18094-117">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="18094-117">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="18094-118">Это свойство доступно, начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="18094-118">This property is available beginning with Windows Installer 5.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="18094-119">Требования</span><span class="sxs-lookup"><span data-stu-id="18094-119">Requirements</span></span>



| <span data-ttu-id="18094-120">Требование</span><span class="sxs-lookup"><span data-stu-id="18094-120">Requirement</span></span> | <span data-ttu-id="18094-121">Значение</span><span class="sxs-lookup"><span data-stu-id="18094-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18094-122">Версия</span><span class="sxs-lookup"><span data-stu-id="18094-122">Version</span></span><br/> | <span data-ttu-id="18094-123">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="18094-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="18094-124">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="18094-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



 

 




