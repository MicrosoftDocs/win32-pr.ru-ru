---
description: Объект Уипревиев используется для просмотра диалоговых окон пользовательского интерфейса и объявлений во время разработки. Этот объект создается методом Енаблеуипревиев объекта Database.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Объект Уипревиев
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675462"
---
# <a name="uipreview-object"></a><span data-ttu-id="2a0c6-104">Объект Уипревиев</span><span class="sxs-lookup"><span data-stu-id="2a0c6-104">UIPreview object</span></span>

<span data-ttu-id="2a0c6-105">Объект **уипревиев** используется для просмотра диалоговых окон пользовательского интерфейса и объявлений во время разработки.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-105">The **UIPreview** object is used to view user interface dialog boxes and billboards during authoring.</span></span> <span data-ttu-id="2a0c6-106">Этот объект создается методом [**енаблеуипревиев**](database-enableuipreview.md) объекта [**Database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="2a0c6-106">This object is created by the [**EnableUIPreview**](database-enableuipreview.md) method of the [**Database**](database-object.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="2a0c6-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="2a0c6-107">Members</span></span>

<span data-ttu-id="2a0c6-108">Объект **уипревиев** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2a0c6-108">The **UIPreview** object has these types of members:</span></span>

-   [<span data-ttu-id="2a0c6-109">Методы</span><span class="sxs-lookup"><span data-stu-id="2a0c6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2a0c6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a0c6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2a0c6-111">Методы</span><span class="sxs-lookup"><span data-stu-id="2a0c6-111">Methods</span></span>

<span data-ttu-id="2a0c6-112">Объект **уипревиев** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-112">The **UIPreview** object has these methods.</span></span>



| <span data-ttu-id="2a0c6-113">Метод</span><span class="sxs-lookup"><span data-stu-id="2a0c6-113">Method</span></span>                                           | <span data-ttu-id="2a0c6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2a0c6-114">Description</span></span>                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a0c6-115">**виевбиллбоард**</span><span class="sxs-lookup"><span data-stu-id="2a0c6-115">**ViewBillboard**</span></span>](uipreview-viewbillboard.md) | <span data-ttu-id="2a0c6-116">Отображает созданное объявление, используя элемент управления ведущего приложения в отображаемом в данный момент диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-116">Displays an authored billboard using the host control in the currently displayed dialog box.</span></span><br/> |
| [<span data-ttu-id="2a0c6-117">**виевдиалог**</span><span class="sxs-lookup"><span data-stu-id="2a0c6-117">**ViewDialog**</span></span>](uipreview-viewdialog.md)       | <span data-ttu-id="2a0c6-118">Отображает диалоговое окно созданного пользовательского интерфейса, сохраненное в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-118">Displays an authored UI dialog box stored in the current database.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="2a0c6-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a0c6-119">Properties</span></span>

<span data-ttu-id="2a0c6-120">Объект **уипревиев** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-120">The **UIPreview** object has these properties.</span></span>



| <span data-ttu-id="2a0c6-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="2a0c6-121">Property</span></span>                                          | <span data-ttu-id="2a0c6-122">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="2a0c6-122">Access type</span></span>           | <span data-ttu-id="2a0c6-123">Описание</span><span class="sxs-lookup"><span data-stu-id="2a0c6-123">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a0c6-124">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="2a0c6-124">**Property**</span></span>](uipreview-property.md)<br/> | <span data-ttu-id="2a0c6-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2a0c6-125">Read/write</span></span><br/> | <span data-ttu-id="2a0c6-126">Представляет строковое значение именованного свойства установщика или значение типа системной переменной среды для текущего процесса, если предваряется знаком процента (%).</span><span class="sxs-lookup"><span data-stu-id="2a0c6-126">Represents the string value of a named installer property or, if prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2a0c6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2a0c6-127">Requirements</span></span>



| <span data-ttu-id="2a0c6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2a0c6-128">Requirement</span></span> | <span data-ttu-id="2a0c6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0c6-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0c6-130">Версия</span><span class="sxs-lookup"><span data-stu-id="2a0c6-130">Version</span></span><br/> | <span data-ttu-id="2a0c6-131">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2a0c6-132">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2a0c6-133">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="2a0c6-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2a0c6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2a0c6-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a0c6-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a0c6-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2a0c6-136">IID</span><span class="sxs-lookup"><span data-stu-id="2a0c6-136">IID</span></span><br/>     | <span data-ttu-id="2a0c6-137">IID \_ иуипревиев определяется как 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2a0c6-137">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="2a0c6-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a0c6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a0c6-139">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="2a0c6-139">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




