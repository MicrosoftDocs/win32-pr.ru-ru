---
description: Установка для свойства ТРАНСФОРМССЕКУРЕ значения 1 информирует установщик о том, что преобразования должны быть кэшированы локально на компьютере пользователя в том месте, где у пользователя нет доступа на запись.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: ТРАНСФОРМССЕКУРЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679933"
---
# <a name="transformssecure-property"></a><span data-ttu-id="5c81d-103">ТРАНСФОРМССЕКУРЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="5c81d-103">TRANSFORMSSECURE property</span></span>

<span data-ttu-id="5c81d-104">Установка для свойства **трансформссекуре** значения 1 информирует установщик о том, что преобразования должны быть кэшированы локально на компьютере пользователя в том месте, где у пользователя нет доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="5c81d-104">Setting the **TRANSFORMSSECURE** property to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="5c81d-105">Задание этого свойства аналогично установке [политики трансформссекуре](transformssecure-policy.md) , за исключением того, что область отличается.</span><span class="sxs-lookup"><span data-stu-id="5c81d-105">Setting this property is like setting the [TransformsSecure policy](transformssecure-policy.md) except that the scope is different.</span></span> <span data-ttu-id="5c81d-106">Настройка политики Трансформссекуре применяется ко всем пакетам, установленным указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5c81d-106">Setting TransformsSecure policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="5c81d-107">Установка свойства **трансформссекуре** применяется к пакету независимо от пользователя.</span><span class="sxs-lookup"><span data-stu-id="5c81d-107">Setting the **TRANSFORMSSECURE** property applies to the package regardless of the user.</span></span>

<span data-ttu-id="5c81d-108">Это свойство предназначено для обеспечения безопасного хранения преобразований с помощью поездок для пользователей Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5c81d-108">The purpose of this property is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="5c81d-109">Если это свойство задано, [Установка обслуживания](maintenance-installation.md) может использовать только преобразование из указанного пути.</span><span class="sxs-lookup"><span data-stu-id="5c81d-109">When this property is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the specified path.</span></span> <span data-ttu-id="5c81d-110">Если путь недоступен, установка обслуживания завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="5c81d-110">If the path is not available the maintenance installation fails.</span></span> <span data-ttu-id="5c81d-111">Таким образом, источник для каждого безопасного преобразования должен находиться в расположении источника установочного пакета.</span><span class="sxs-lookup"><span data-stu-id="5c81d-111">A source for each secure transform must therefore reside at the location of the source of the installation package.</span></span> <span data-ttu-id="5c81d-112">Затем, если установщик обнаружит, что преобразование отсутствует на локальном компьютере, оно может восстановить преобразование из этого источника.</span><span class="sxs-lookup"><span data-stu-id="5c81d-112">Then if the installer finds that the transform is missing on the local computer, it can restore the transform from this source.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c81d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c81d-113">Remarks</span></span>

<span data-ttu-id="5c81d-114">Установщик Windows интерпретирует свойство [**трансформсатсаурце**](transformsatsource.md) так, чтобы оно совпадало со свойством **трансформссекуре** .</span><span class="sxs-lookup"><span data-stu-id="5c81d-114">Windows Installer interprets the [**TRANSFORMSATSOURCE**](transformsatsource.md) property to be the same as the **TRANSFORMSSECURE** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c81d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5c81d-115">Requirements</span></span>



| <span data-ttu-id="5c81d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5c81d-116">Requirement</span></span> | <span data-ttu-id="5c81d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5c81d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c81d-118">Версия</span><span class="sxs-lookup"><span data-stu-id="5c81d-118">Version</span></span><br/> | <span data-ttu-id="5c81d-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c81d-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5c81d-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5c81d-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5c81d-121">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c81d-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5c81d-122">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5c81d-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c81d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="5c81d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c81d-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c81d-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5c81d-125">Преобразования баз данных</span><span class="sxs-lookup"><span data-stu-id="5c81d-125">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




