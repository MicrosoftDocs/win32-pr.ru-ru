---
description: Во время параллельной установки установщик задает для свойства Парентпродукткоде в сеансе параллельной установки то же значение, что и свойство ProductCode в сеансе установки родительской системы.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: Парентпродукткоде, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82385a4df94d3a044f0ee6a77461d69e63cc6d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652039"
---
# <a name="parentproductcode-property"></a><span data-ttu-id="2a7f1-103">Парентпродукткоде, свойство</span><span class="sxs-lookup"><span data-stu-id="2a7f1-103">ParentProductCode property</span></span>

<span data-ttu-id="2a7f1-104">Во время параллельной установки установщик задает для свойства **парентпродукткоде** в сеансе параллельной установки то же значение, что и свойство [**ProductCode**](productcode.md) в сеансе установки родительской системы.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-104">During a concurrent installation, the installer sets the **ParentProductCode** property in the concurrent installation's session to the same value as the [**ProductCode**](productcode.md) property in the parent installation's session.</span></span> <span data-ttu-id="2a7f1-105">Родительские установки выполняют параллельные действия установки для выполнения параллельной установки.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-105">Parent installations run the concurrent installation actions to perform a concurrent installation.</span></span> <span data-ttu-id="2a7f1-106">Пакет установки может определить, выполняется ли параллельное действие установки, путем проверки значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-106">An installation package can determine whether it is being installed by a concurrent installation action by checking the value of this property.</span></span>

> [!Note]  
> <span data-ttu-id="2a7f1-107">Параллельные установки не рекомендуются для установки приложений, предназначенных для выпуска в общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-107">Concurrent Installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="2a7f1-108">Сведения о параллельных установках см. в разделе [одновременная установка](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="2a7f1-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="2a7f1-109">Это свойство не задано, если параллельная установка выполняется действием [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2a7f1-109">This property is not set if the concurrent installation is being run by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="2a7f1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a7f1-110">Remarks</span></span>

<span data-ttu-id="2a7f1-111">Чтобы предотвратить установку пакета в качестве параллельной установки, добавьте в таблицу [лаунчкондитион](launchcondition-table.md) одну из следующих условных операторов.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-111">To prevent a package from ever being installed as a concurrent installation, add either of the following conditional statements to the [LaunchCondition](launchcondition-table.md) table.</span></span> <span data-ttu-id="2a7f1-112">Это предотвращает установку пакета в ходе параллельной установки, выполняемой другой установкой.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-112">This prevents the package from ever being installed by a concurrent installation action run by another installation.</span></span> <span data-ttu-id="2a7f1-113">Это не мешает установке пакета с помощью действия [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2a7f1-113">This does not prevent the package from being installed by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a><span data-ttu-id="2a7f1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2a7f1-114">Requirements</span></span>



| <span data-ttu-id="2a7f1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2a7f1-115">Requirement</span></span> | <span data-ttu-id="2a7f1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2a7f1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7f1-117">Версия</span><span class="sxs-lookup"><span data-stu-id="2a7f1-117">Version</span></span><br/> | <span data-ttu-id="2a7f1-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2a7f1-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2a7f1-120">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a7f1-120">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2a7f1-121">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2a7f1-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a7f1-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2a7f1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7f1-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a7f1-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="2a7f1-124">**паренторигиналдатабасе**</span><span class="sxs-lookup"><span data-stu-id="2a7f1-124">**ParentOriginalDatabase**</span></span>](parentoriginaldatabase.md)
</dt> </dl>

 

 




