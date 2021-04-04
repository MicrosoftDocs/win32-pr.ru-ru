---
description: Действие Ремовеинивалуес удаляет сведения из ini-файла, указанные для удаления в таблице Ремовеинифиле, если компонент настроен на локальную установку или запуск из исходного кода.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Действие Ремовеинивалуес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999517"
---
# <a name="removeinivalues-action"></a><span data-ttu-id="9504e-103">Действие Ремовеинивалуес</span><span class="sxs-lookup"><span data-stu-id="9504e-103">RemoveIniValues Action</span></span>

<span data-ttu-id="9504e-104">Действие Ремовеинивалуес удаляет сведения из ini-файла, указанные для удаления в [таблице ремовеинифиле](removeinifile-table.md) , если компонент настроен на локальную установку или запуск из исходного кода.</span><span class="sxs-lookup"><span data-stu-id="9504e-104">The RemoveIniValues action removes .ini file information specified for removal in the [RemoveIniFile table](removeinifile-table.md) if the component is set to be installed locally or run-from-source.</span></span> <span data-ttu-id="9504e-105">Действие Ремовеинивалуес удаляет данные ini-файла, связанные с компонентом в [таблице инифиле](inifile-table.md).</span><span class="sxs-lookup"><span data-stu-id="9504e-105">The RemoveIniValues action removes .ini file information that has been associated with a component in the [IniFile table](inifile-table.md).</span></span> <span data-ttu-id="9504e-106">Это действие также удаляет сведения из ini-файла, если данные были записаны [действием вритеинивалуес](writeinivalues-action.md) и запланировано удаление компонента.</span><span class="sxs-lookup"><span data-stu-id="9504e-106">This action also removes .ini file information if the information was written by the [WriteIniValues action](writeinivalues-action.md) and the component is scheduled to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9504e-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="9504e-107">Sequence Restrictions</span></span>

<span data-ttu-id="9504e-108">Действие [инсталлвалидате](installvalidate-action.md) должно быть вызвано перед действием ремовеинивалуес.</span><span class="sxs-lookup"><span data-stu-id="9504e-108">The [InstallValidate](installvalidate-action.md) action must be called before the RemoveIniValues action.</span></span> <span data-ttu-id="9504e-109">Если в последовательности используется действие [вритеинивалуес](writeinivalues-action.md) , оно должно появиться после ремовеинивалуес.</span><span class="sxs-lookup"><span data-stu-id="9504e-109">If a [WriteIniValues](writeinivalues-action.md) action is used in the sequence, it must appear after RemoveIniValues.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9504e-110">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="9504e-110">ActionData Messages</span></span>



| <span data-ttu-id="9504e-111">Поле</span><span class="sxs-lookup"><span data-stu-id="9504e-111">Field</span></span> | <span data-ttu-id="9504e-112">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="9504e-112">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="9504e-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9504e-113">\[1\]</span></span> | <span data-ttu-id="9504e-114">Идентификатор ini-файла.</span><span class="sxs-lookup"><span data-stu-id="9504e-114">Identifier of .ini file.</span></span>      |
| <span data-ttu-id="9504e-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="9504e-115">\[2\]</span></span> | <span data-ttu-id="9504e-116">Раздел Key. ini-файла.</span><span class="sxs-lookup"><span data-stu-id="9504e-116">An .ini file key section.</span></span>     |
| <span data-ttu-id="9504e-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="9504e-117">\[3\]</span></span> | <span data-ttu-id="9504e-118">Элемент удален из ini-файла.</span><span class="sxs-lookup"><span data-stu-id="9504e-118">Item removed from .ini file.</span></span>  |
| <span data-ttu-id="9504e-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="9504e-119">\[4\]</span></span> | <span data-ttu-id="9504e-120">Значение, удаленное из ini-файла.</span><span class="sxs-lookup"><span data-stu-id="9504e-120">Value removed from .ini file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9504e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9504e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9504e-122">Таблица Ремовеинифиле</span><span class="sxs-lookup"><span data-stu-id="9504e-122">RemoveIniFile table</span></span>](removeinifile-table.md)
</dt> <dt>

[<span data-ttu-id="9504e-123">Таблица Инифиле</span><span class="sxs-lookup"><span data-stu-id="9504e-123">IniFile table</span></span>](inifile-table.md)
</dt> <dt>

[<span data-ttu-id="9504e-124">Действие Вритеинивалуес</span><span class="sxs-lookup"><span data-stu-id="9504e-124">WriteIniValues action</span></span>](writeinivalues-action.md)
</dt> <dt>

[<span data-ttu-id="9504e-125">инсталлвалидате</span><span class="sxs-lookup"><span data-stu-id="9504e-125">InstallValidate</span></span>](installvalidate-action.md)
</dt> </dl>

 

 



