---
description: Значение свойства ProductVersion — это версия продукта в строковом формате.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: ProductVersion, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652066"
---
# <a name="productversion-property"></a><span data-ttu-id="9467e-103">ProductVersion, свойство</span><span class="sxs-lookup"><span data-stu-id="9467e-103">ProductVersion property</span></span>

<span data-ttu-id="9467e-104">Значение свойства **ProductVersion** — это версия продукта в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="9467e-104">The value of the **ProductVersion** property is the version of the product in string format.</span></span> <span data-ttu-id="9467e-105">Это свойство является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9467e-105">This property is REQUIRED.</span></span>

<span data-ttu-id="9467e-106">Формат строки выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9467e-106">The format of the string is as follows:</span></span>

<dl> <span data-ttu-id="9467e-107">ОсновнойНомерВерсии.ДополнительныйНомерВерсии.НомерПостроения</span><span class="sxs-lookup"><span data-stu-id="9467e-107">major.minor.build</span></span>  
</dl>

<span data-ttu-id="9467e-108">Первое поле является основной версией и имеет максимальное значение 255.</span><span class="sxs-lookup"><span data-stu-id="9467e-108">The first field is the major version and has a maximum value of 255.</span></span> <span data-ttu-id="9467e-109">Второе поле является дополнительным номером версии и имеет максимальное значение 255.</span><span class="sxs-lookup"><span data-stu-id="9467e-109">The second field is the minor version and has a maximum value of 255.</span></span> <span data-ttu-id="9467e-110">Третье поле называется версией сборки или версией обновления и имеет максимальное значение 65 535.</span><span class="sxs-lookup"><span data-stu-id="9467e-110">The third field is called the build version or the update version and has a maximum value of 65,535.</span></span>

## <a name="remarks"></a><span data-ttu-id="9467e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9467e-111">Remarks</span></span>

<span data-ttu-id="9467e-112">По крайней мере одно из трех полей **ProductVersion** должно измениться для обновления с помощью [таблицы обновления](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="9467e-112">At least one of the three fields of **ProductVersion** must change for an upgrade using the [Upgrade table](upgrade-table.md).</span></span> <span data-ttu-id="9467e-113">Любое обновление, которое изменяет только код пакета, но оставляет **ProductVersion** и [**ProductCode**](productcode.md) без изменений, называется [небольшим обновлением](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="9467e-113">Any update that changes only the package code, but leaves **ProductVersion** and [**ProductCode**](productcode.md) unchanged is called a [small update](small-updates.md).</span></span> <span data-ttu-id="9467e-114">Три поля версий предоставляются в первую очередь для удобства.</span><span class="sxs-lookup"><span data-stu-id="9467e-114">The three versions fields are provided primarily for convenience.</span></span> <span data-ttu-id="9467e-115">Например, если вы хотите изменить **ProductVersion**, но не хотите изменять основную или дополнительную версии, можно изменить версию сборки.</span><span class="sxs-lookup"><span data-stu-id="9467e-115">For example, if you want to change **ProductVersion**, but do not want to change either the major or minor versions, you can change the build version.</span></span>

<span data-ttu-id="9467e-116">Обратите внимание, что установщик Windows использует только первые три поля версии продукта.</span><span class="sxs-lookup"><span data-stu-id="9467e-116">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="9467e-117">Если включить в версию продукта четвертое поле, установщик игнорирует четвертое поле.</span><span class="sxs-lookup"><span data-stu-id="9467e-117">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

## <a name="requirements"></a><span data-ttu-id="9467e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9467e-118">Requirements</span></span>



| <span data-ttu-id="9467e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9467e-119">Requirement</span></span> | <span data-ttu-id="9467e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9467e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9467e-121">Версия</span><span class="sxs-lookup"><span data-stu-id="9467e-121">Version</span></span><br/> | <span data-ttu-id="9467e-122">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9467e-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9467e-123">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9467e-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9467e-124">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9467e-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9467e-125">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9467e-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9467e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9467e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9467e-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="9467e-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9467e-128">Установка исправлений и обновления</span><span class="sxs-lookup"><span data-stu-id="9467e-128">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="9467e-129">небольшое обновление</span><span class="sxs-lookup"><span data-stu-id="9467e-129">small update</span></span>](small-updates.md)
</dt> </dl>

 

 




