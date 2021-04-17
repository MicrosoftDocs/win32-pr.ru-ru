---
description: Свойство "Сводка по количеству страниц" содержит минимальную версию установщика, необходимую для пакета установки.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Свойство сводки количества страниц
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652041"
---
# <a name="page-count-summary-property"></a><span data-ttu-id="1d419-103">Свойство сводки количества страниц</span><span class="sxs-lookup"><span data-stu-id="1d419-103">Page Count Summary property</span></span>

<span data-ttu-id="1d419-104">Свойство " **Сводка по количеству страниц** " содержит минимальную версию установщика, необходимую для пакета установки.</span><span class="sxs-lookup"><span data-stu-id="1d419-104">The **Page Count Summary** property contains the minimum installer version required by the installation package.</span></span> <span data-ttu-id="1d419-105">Как минимум установщик Windows 2,0, этому свойству должно быть присвоено целое число 200.</span><span class="sxs-lookup"><span data-stu-id="1d419-105">For a minimum of Windows Installer 2.0, this property must be set to the integer 200.</span></span> <span data-ttu-id="1d419-106">Как минимум установщик Windows 3,0, этому свойству должно быть присвоено целое число 300.</span><span class="sxs-lookup"><span data-stu-id="1d419-106">For a minimum of Windows Installer 3.0, this property must be set to the integer 300.</span></span> <span data-ttu-id="1d419-107">Для минимума установщик Windows 3,1 это свойство должно иметь значение 301.</span><span class="sxs-lookup"><span data-stu-id="1d419-107">For a minimum of Windows Installer 3.1, this property must be set to 301.</span></span> <span data-ttu-id="1d419-108">Для минимума установщик Windows 4,5 это свойство должно иметь значение 405.</span><span class="sxs-lookup"><span data-stu-id="1d419-108">For a minimum of Windows Installer 4.5, this property must be set to 405.</span></span> <span data-ttu-id="1d419-109">Для минимума установщик Windows 5,0 это свойство должно иметь значение 500.</span><span class="sxs-lookup"><span data-stu-id="1d419-109">For a minimum of Windows Installer 5.0, this property must be set to 500.</span></span>

<span data-ttu-id="1d419-110">Для [64-разрядных пакетов установщик Windows](64-bit-windows-installer-packages.md)этому свойству должно быть присвоено целое число 200 или выше.</span><span class="sxs-lookup"><span data-stu-id="1d419-110">For [64-bit Windows Installer Packages](64-bit-windows-installer-packages.md), this property must be set to the integer 200 or greater.</span></span> <span data-ttu-id="1d419-111">Для 64-разрядных пакетов установщик Windows на платформе Arm64 этому свойству должно быть присвоено целое число 500 или выше.</span><span class="sxs-lookup"><span data-stu-id="1d419-111">For 64-bit Windows Installer Packages on the Arm64 platform, this property must be set to the integer 500 or greater.</span></span>

<span data-ttu-id="1d419-112">Для пакета преобразования свойство **Сводка количества страниц** содержит минимальную версию установщика, необходимую для обработки преобразования.</span><span class="sxs-lookup"><span data-stu-id="1d419-112">For a transform package, the **Page Count Summary** property contains the minimum installer version required to process the transform.</span></span> <span data-ttu-id="1d419-113">Задает большее из двух значений свойств **сводки количества страниц** , принадлежащих к базам данных, используемым для создания преобразования.</span><span class="sxs-lookup"><span data-stu-id="1d419-113">Set to the greater of the two **Page Count Summary** property values that belong to the databases used to generate the transform.</span></span>

<span data-ttu-id="1d419-114">Для пакета исправлений свойство сводка по **количеству страниц** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="1d419-114">For a patch package, the **Page Count Summary** property is set to Null.</span></span>

<span data-ttu-id="1d419-115">Это свойство сводки является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1d419-115">This summary property is required.</span></span>

<span data-ttu-id="1d419-116">Это свойство можно использовать для создания пакета, который может быть установлен только в указанной минимальной или более поздней версии установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="1d419-116">This property can be used to author a package that can be installed only by the specified minimum or later version of the Windows Installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d419-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1d419-117">Requirements</span></span>



| <span data-ttu-id="1d419-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1d419-118">Requirement</span></span> | <span data-ttu-id="1d419-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1d419-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d419-120">Версия</span><span class="sxs-lookup"><span data-stu-id="1d419-120">Version</span></span><br/> | <span data-ttu-id="1d419-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d419-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1d419-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d419-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1d419-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d419-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d419-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d419-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d419-125">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="1d419-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




