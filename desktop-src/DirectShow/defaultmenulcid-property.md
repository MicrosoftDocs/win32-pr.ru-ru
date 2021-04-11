---
description: Свойство Двдадм. ДефаултменулЦид задает или получает параметр реестра для указанного пользователем языка по умолчанию для меню.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: ДефаултменулЦид, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140435"
---
# <a name="defaultmenulcid-property"></a><span data-ttu-id="0f21e-103">ДефаултменулЦид, свойство</span><span class="sxs-lookup"><span data-stu-id="0f21e-103">DefaultMenuLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="0f21e-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0f21e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0f21e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0f21e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0f21e-106">`DVDAdm.DefaultMenuLCID`Свойство задает или получает параметр реестра для указанного пользователем языка по умолчанию для меню.</span><span class="sxs-lookup"><span data-stu-id="0f21e-106">The `DVDAdm.DefaultMenuLCID` property sets or retrieves the registry setting for the user-specified default LCID for menus.</span></span>

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a><span data-ttu-id="0f21e-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f21e-107">Return Value</span></span>

<span data-ttu-id="0f21e-108">Возвращает целочисленное значение, представляющее код языка, сохраненный в параметрах реестра для приложения DVD.</span><span class="sxs-lookup"><span data-stu-id="0f21e-108">Returns an Integer value representing the LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="0f21e-109">Это значение не обязательно совпадает с языком меню по умолчанию, созданным на DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="0f21e-109">This value is not necessarily the same as the default menu language as authored on the DVD.</span></span> <span data-ttu-id="0f21e-110">Диапазон допустимых кодов языка см. в документации по Win32 в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="0f21e-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f21e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f21e-111">Remarks</span></span>

<span data-ttu-id="0f21e-112">Это свойство доступно для чтения и записи и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f21e-112">This property is read/write with no default value.</span></span> <span data-ttu-id="0f21e-113">Если не указан LCID меню по умолчанию, объект Мсдвдадм будет использовать язык, помеченный как язык меню по умолчанию на диске.</span><span class="sxs-lookup"><span data-stu-id="0f21e-113">If no default menu LCID is specified, the MSDVDAdm object will use the language that is marked as the default menu language on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f21e-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f21e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f21e-115">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="0f21e-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



