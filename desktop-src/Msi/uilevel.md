---
description: Установщик задает для свойства Duilevel уровень пользовательского интерфейса.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Duilevel, свойство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675463"
---
# <a name="uilevel-property"></a><span data-ttu-id="de9bc-103">Duilevel, свойство</span><span class="sxs-lookup"><span data-stu-id="de9bc-103">UILevel property</span></span>

<span data-ttu-id="de9bc-104">Установщик задает для свойства **duilevel** уровень пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="de9bc-104">The installer sets the **UILevel** property to the level of the user interface.</span></span> <span data-ttu-id="de9bc-105">Внутренний пользовательский интерфейс включается и задается параметром [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="de9bc-105">The internal UI is enabled and set by [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="de9bc-106">Для этого свойства задан один из следующих типов данных ИНСТАЛЛУИЛЕВЕЛ.</span><span class="sxs-lookup"><span data-stu-id="de9bc-106">This property is set to one of the following INSTALLUILEVEL data types.</span></span>



| <span data-ttu-id="de9bc-107">инсталлуилевел</span><span class="sxs-lookup"><span data-stu-id="de9bc-107">INSTALLUILEVEL</span></span>          | <span data-ttu-id="de9bc-108">Числовое значение</span><span class="sxs-lookup"><span data-stu-id="de9bc-108">Numeric value</span></span> | <span data-ttu-id="de9bc-109">Уровень пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="de9bc-109">User interface level</span></span>                        |
|-------------------------|---------------|---------------------------------------------|
| <span data-ttu-id="de9bc-110">ИНСТАЛЛУИЛЕВЕЛ \_ None</span><span class="sxs-lookup"><span data-stu-id="de9bc-110">INSTALLUILEVEL\_NONE</span></span>    | <span data-ttu-id="de9bc-111">2</span><span class="sxs-lookup"><span data-stu-id="de9bc-111">2</span></span>             | <span data-ttu-id="de9bc-112">Полностью автоматическая установка.</span><span class="sxs-lookup"><span data-stu-id="de9bc-112">Completely silent installation.</span></span>             |
| <span data-ttu-id="de9bc-113">ИНСТАЛЛУИЛЕВЕЛ \_ Basic</span><span class="sxs-lookup"><span data-stu-id="de9bc-113">INSTALLUILEVEL\_BASIC</span></span>   | <span data-ttu-id="de9bc-114">3</span><span class="sxs-lookup"><span data-stu-id="de9bc-114">3</span></span>             | <span data-ttu-id="de9bc-115">Простой ход выполнения и обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="de9bc-115">Simple progress and error handling.</span></span>         |
| <span data-ttu-id="de9bc-116">ИНСТАЛЛУИЛЕВЕЛ \_ уменьшилось</span><span class="sxs-lookup"><span data-stu-id="de9bc-116">INSTALLUILEVEL\_REDUCED</span></span> | <span data-ttu-id="de9bc-117">4</span><span class="sxs-lookup"><span data-stu-id="de9bc-117">4</span></span>             | <span data-ttu-id="de9bc-118">Разработанный пользовательский интерфейс, диалоговые окна мастера подавляются.</span><span class="sxs-lookup"><span data-stu-id="de9bc-118">Authored UI, wizard dialogs suppressed.</span></span>     |
| <span data-ttu-id="de9bc-119">ИНСТАЛЛУИЛЕВЕЛ \_ Full</span><span class="sxs-lookup"><span data-stu-id="de9bc-119">INSTALLUILEVEL\_FULL</span></span>    | <span data-ttu-id="de9bc-120">5</span><span class="sxs-lookup"><span data-stu-id="de9bc-120">5</span></span>             | <span data-ttu-id="de9bc-121">Создан пользовательский интерфейс с мастерами, ходом выполнения, ошибками.</span><span class="sxs-lookup"><span data-stu-id="de9bc-121">Authored UI with wizards, progress, errors.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="de9bc-122">Требования</span><span class="sxs-lookup"><span data-stu-id="de9bc-122">Requirements</span></span>



| <span data-ttu-id="de9bc-123">Требование</span><span class="sxs-lookup"><span data-stu-id="de9bc-123">Requirement</span></span> | <span data-ttu-id="de9bc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="de9bc-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de9bc-125">Версия</span><span class="sxs-lookup"><span data-stu-id="de9bc-125">Version</span></span><br/> | <span data-ttu-id="de9bc-126">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="de9bc-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="de9bc-127">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="de9bc-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="de9bc-128">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="de9bc-128">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="de9bc-129">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="de9bc-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de9bc-130">См. также</span><span class="sxs-lookup"><span data-stu-id="de9bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9bc-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="de9bc-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="de9bc-132">Пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="de9bc-132">User Interface</span></span>](user-interface.md)
</dt> <dt>

[<span data-ttu-id="de9bc-133">Определение уровня пользовательского интерфейса на основе настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="de9bc-133">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




