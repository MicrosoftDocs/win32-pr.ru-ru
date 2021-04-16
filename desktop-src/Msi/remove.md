---
description: Значение свойства Remove представляет собой список функций, разделенных запятыми, которые необходимо удалить.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE, свойство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652185"
---
# <a name="remove-property"></a><span data-ttu-id="587e6-103">REMOVE, свойство</span><span class="sxs-lookup"><span data-stu-id="587e6-103">REMOVE property</span></span>

<span data-ttu-id="587e6-104">Значение свойства **Remove** представляет собой список функций, разделенных запятыми, которые необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="587e6-104">The value of the **REMOVE** property is a list of features delimited by commas that are to be removed.</span></span> <span data-ttu-id="587e6-105">Функции должны присутствовать в столбце Feature [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="587e6-105">The features must be present in the Feature column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="587e6-106">Обратите внимание, что при использовании команды Remove = ALL в командной строке установщик удаляет все компоненты, уровень установки которых больше 0.</span><span class="sxs-lookup"><span data-stu-id="587e6-106">Note that if you use REMOVE=ALL on the command line, the installer removes all features having an install level greater than 0.</span></span> <span data-ttu-id="587e6-107">В этом случае установщик не удаляет компоненты, уровень установки которых равен 0.</span><span class="sxs-lookup"><span data-stu-id="587e6-107">In this case, the installer does not remove features having an install level of 0.</span></span> <span data-ttu-id="587e6-108">Дополнительные сведения об уровне установки компонентов см. в разделе [Таблица функций](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="587e6-108">For more information about the install level of features see [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="587e6-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="587e6-109">Remarks</span></span>

<span data-ttu-id="587e6-110">Чтобы определить, был ли установлен продукт полностью удален, автор пакета может использовать условное выражение для проверки того, является ли Remove = ALL.</span><span class="sxs-lookup"><span data-stu-id="587e6-110">To determine whether a product has been set to be completely uninstalled, a package author may use a conditional expression to check whether REMOVE=ALL.</span></span> <span data-ttu-id="587e6-111">Обратите внимание, что если продукт удаляется из-за того, что его компонент Top имеет значение отсутствует, свойство **Remove** может не равняться ALL до [действия инсталлвалидате](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="587e6-111">Note that if the product is removed by setting its top feature to absent, the **REMOVE** property may not equal ALL until after the [InstallValidate action](installvalidate-action.md).</span></span> <span data-ttu-id="587e6-112">Это означает, что любое пользовательское действие, которое зависит от Remove = ALL, должно быть упорядочено после Инсталлвалидате.</span><span class="sxs-lookup"><span data-stu-id="587e6-112">This means that any custom action that depends upon REMOVE=ALL must be sequenced after the InstallValidate.</span></span> <span data-ttu-id="587e6-113">Дополнительные сведения см. [в разделе условия выполнения действий при удалении](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="587e6-113">For more information see also [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span> <span data-ttu-id="587e6-114">Обратите внимание, что в именах функций учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="587e6-114">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="587e6-115">Установщик всегда вычисляет следующие свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="587e6-115">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="587e6-116">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="587e6-116">**ADDLOCAL**</span></span>](addlocal.md)
2.  <span data-ttu-id="587e6-117">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="587e6-117">**REMOVE**</span></span>
3.  [<span data-ttu-id="587e6-118">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="587e6-118">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="587e6-119">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="587e6-119">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="587e6-120">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="587e6-120">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="587e6-121">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="587e6-121">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="587e6-122">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="587e6-122">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="587e6-123">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="587e6-123">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="587e6-124">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="587e6-124">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="587e6-125">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="587e6-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="587e6-126">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="587e6-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="587e6-127">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="587e6-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="587e6-128">Например, если в командной строке указано значение ADDLOCAL = ALL, АДДСАУРЦЕ = Мифеатуре, то все функции сначала устанавливаются в локальный режим, а затем Мифеатуре устанавливается в режим запуска от исходного кода.</span><span class="sxs-lookup"><span data-stu-id="587e6-128">For example, if the command line specifies ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="587e6-129">Если командная строка имеет значение АДДСАУРЦЕ = ALL, ADDLOCAL = Мифеатуре, то первый Мифеатуре имеет значение Local, а затем, когда вычисляется АДДСАУРЦЕ = ALL, все функции (включая Мифеатуре) сбрасываются в состояние запуска от исходного кода.</span><span class="sxs-lookup"><span data-stu-id="587e6-129">If the command line is ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="587e6-130">Установщик задает для свойства предварительно [**выбранных**](preselected.md) значений значение "1" во время возобновления приостановленной установки или при указании любого из указанных выше свойств в командной строке.</span><span class="sxs-lookup"><span data-stu-id="587e6-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="587e6-131">Требования</span><span class="sxs-lookup"><span data-stu-id="587e6-131">Requirements</span></span>



| <span data-ttu-id="587e6-132">Требование</span><span class="sxs-lookup"><span data-stu-id="587e6-132">Requirement</span></span> | <span data-ttu-id="587e6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="587e6-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="587e6-134">Версия</span><span class="sxs-lookup"><span data-stu-id="587e6-134">Version</span></span><br/> | <span data-ttu-id="587e6-135">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="587e6-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="587e6-136">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="587e6-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="587e6-137">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="587e6-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="587e6-138">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="587e6-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="587e6-139">См. также</span><span class="sxs-lookup"><span data-stu-id="587e6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587e6-140">Свойства</span><span class="sxs-lookup"><span data-stu-id="587e6-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




