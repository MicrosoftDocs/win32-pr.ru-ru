---
description: Свойство Дефаултуифонт задает стиль шрифта по умолчанию, используемый для элементов управления. Чтобы указать значение по умолчанию, задайте Дефаултуифонт в качестве одного из стандартных стилей в таблице система создала шрифт в таблице свойств.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Дефаултуифонт, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652296"
---
# <a name="defaultuifont-property"></a><span data-ttu-id="92b45-104">Дефаултуифонт, свойство</span><span class="sxs-lookup"><span data-stu-id="92b45-104">DefaultUIFont property</span></span>

<span data-ttu-id="92b45-105">Свойство **дефаултуифонт** задает стиль шрифта по умолчанию, используемый для элементов управления.</span><span class="sxs-lookup"><span data-stu-id="92b45-105">The **DefaultUIFont** property sets the default font style used for controls.</span></span> <span data-ttu-id="92b45-106">Чтобы указать значение по умолчанию, задайте **дефаултуифонт** в качестве одного из стандартных стилей в [таблице система создала шрифт](textstyle-table.md) в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="92b45-106">To specify the default, set **DefaultUIFont** to one of the predefined styles in the [TextStyle table](textstyle-table.md) in the [Property table](property-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92b45-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92b45-107">Remarks</span></span>

<span data-ttu-id="92b45-108">Свойство **дефаултуифонт** каждого пакета установки с пользовательским интерфейсом должно быть установлено в [таблице свойств](property-table.md) на один из стандартных стилей, перечисленных в [таблице система создала шрифт](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="92b45-108">The **DefaultUIFont** property of every installation package with a UI should be set in the [Property table](property-table.md) to one of the predefined styles listed in the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="92b45-109">Если это свойство не указано, установщик использует системный шрифт.</span><span class="sxs-lookup"><span data-stu-id="92b45-109">If this property is not specified, the installer uses the System font.</span></span> <span data-ttu-id="92b45-110">Это может привести к неправильному отображению текстовых строк в установщике, если кодовая страница пакета отличается от кодовой страницы пользовательского интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92b45-110">This can cause the installer to improperly display text strings when the package's code page is different from the user's default UI code page.</span></span>

<span data-ttu-id="92b45-111">Текст и стиль шрифта элемента управления можно задать, как описано в разделе [Добавление элементов управления и текста](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="92b45-111">The text and font style of a control can be set as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="92b45-112">Если символьная строка, указанная в столбце text [таблицы управления](control-table.md) или [ббконтрол](bbcontrol-table.md) , не указывает стиль шрифта, элемент управления использует значение свойства **дефаултуифонт** в качестве стиля шрифта.</span><span class="sxs-lookup"><span data-stu-id="92b45-112">If the character string listed in the Text column of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) does not specify the font style, the control uses the value of the **DefaultUIFont** property as the font style.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b45-113">Требования</span><span class="sxs-lookup"><span data-stu-id="92b45-113">Requirements</span></span>



| <span data-ttu-id="92b45-114">Требование</span><span class="sxs-lookup"><span data-stu-id="92b45-114">Requirement</span></span> | <span data-ttu-id="92b45-115">Значение</span><span class="sxs-lookup"><span data-stu-id="92b45-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b45-116">Версия</span><span class="sxs-lookup"><span data-stu-id="92b45-116">Version</span></span><br/> | <span data-ttu-id="92b45-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92b45-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="92b45-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92b45-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="92b45-119">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="92b45-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="92b45-120">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="92b45-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92b45-121">См. также</span><span class="sxs-lookup"><span data-stu-id="92b45-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b45-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="92b45-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




