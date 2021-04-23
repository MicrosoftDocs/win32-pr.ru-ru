---
description: ICE07 проверяет, что установочный пакет указывает, что шрифты должны быть установлены в Фонтсфолдер. Если шрифт устанавливается в папку, отличную от Фонтсфолдер, установщик создает ярлык вместо фактической установки шрифта.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650934"
---
# <a name="ice07"></a><span data-ttu-id="a460d-104">ICE07</span><span class="sxs-lookup"><span data-stu-id="a460d-104">ICE07</span></span>

<span data-ttu-id="a460d-105">ICE07 проверяет, что установочный пакет указывает, что шрифты должны быть установлены в Фонтсфолдер.</span><span class="sxs-lookup"><span data-stu-id="a460d-105">ICE07 validates that installation package specifies that fonts be installed into the FontsFolder.</span></span> <span data-ttu-id="a460d-106">Если шрифт устанавливается в папку, отличную от Фонтсфолдер, установщик создает ярлык вместо фактической установки шрифта.</span><span class="sxs-lookup"><span data-stu-id="a460d-106">If a font is installed to a folder other than the FontsFolder the installer creates a shortcut rather than actually installing the font.</span></span>

<span data-ttu-id="a460d-107">Настраиваемое действие ICE07 выполняет следующие действия для каждого шрифта в [таблице Font](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="a460d-107">The ICE07 custom action does the following for each font in the [Font table](font-table.md).</span></span>

1.  <span data-ttu-id="a460d-108">Находит файл шрифта, к которому относится каждое название шрифта, с помощью [таблицы Font](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="a460d-108">Finds the font file to which each font title belongs using the [Font table](font-table.md).</span></span>
2.  <span data-ttu-id="a460d-109">Запрашивает \_ столбец компонента [таблицы File](file-table.md) для компонента, управляющего каждым файлом.</span><span class="sxs-lookup"><span data-stu-id="a460d-109">Queries the Component\_ column of the [File table](file-table.md) for the component that controls each file.</span></span>
3.  <span data-ttu-id="a460d-110">Запрашивает \_ столбец каталога [таблицы Component](component-table.md) , чтобы получить ключ в таблице каталога.</span><span class="sxs-lookup"><span data-stu-id="a460d-110">Queries the Directory\_ column of the [Component table](component-table.md) to obtain a key into the Directory table.</span></span>
4.  <span data-ttu-id="a460d-111">Разрешает [таблицу Directory](directory-table.md) , чтобы определить имя папки, в которую установщик должен установить файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="a460d-111">Resolves the [Directory table](directory-table.md) to determine the name of the folder into which the installer is to install the font file</span></span>
5.  <span data-ttu-id="a460d-112">Отправляет сообщение об ошибке, если файл шрифта устанавливается в папку, отличную от Фонтсфолдер.</span><span class="sxs-lookup"><span data-stu-id="a460d-112">Posts an error if the font file is being installed into a folder other than the FontsFolder.</span></span>

## <a name="result"></a><span data-ttu-id="a460d-113">Результат</span><span class="sxs-lookup"><span data-stu-id="a460d-113">Result</span></span>

<span data-ttu-id="a460d-114">ICE07 отправляет сообщение об ошибке, если обнаруживает, что база данных указывает, что файл шрифта должен быть установлен в папку, отличную от Фонтсфолдер.</span><span class="sxs-lookup"><span data-stu-id="a460d-114">ICE07 posts an error if it finds that the database specifies that a font file be installed into a folder other than the FontsFolder.</span></span>

## <a name="example"></a><span data-ttu-id="a460d-115">Пример</span><span class="sxs-lookup"><span data-stu-id="a460d-115">Example</span></span>

<span data-ttu-id="a460d-116">IC07 выводит следующее сообщение об ошибке для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="a460d-116">IC07 would post the following error message for the example shown.</span></span>

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[<span data-ttu-id="a460d-117">Таблица шрифтов</span><span class="sxs-lookup"><span data-stu-id="a460d-117">Font Table</span></span>](font-table.md)



| <span data-ttu-id="a460d-118">Файл\_</span><span class="sxs-lookup"><span data-stu-id="a460d-118">File\_</span></span> | <span data-ttu-id="a460d-119">фонттитле</span><span class="sxs-lookup"><span data-stu-id="a460d-119">FontTitle</span></span> |
|--------|-----------|
| <span data-ttu-id="a460d-120">миртле</span><span class="sxs-lookup"><span data-stu-id="a460d-120">Myrtle</span></span> | <span data-ttu-id="a460d-121">Tahoma</span><span class="sxs-lookup"><span data-stu-id="a460d-121">Tahoma</span></span>    |



 

<span data-ttu-id="a460d-122">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a460d-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="a460d-123">Файл</span><span class="sxs-lookup"><span data-stu-id="a460d-123">File</span></span>   | <span data-ttu-id="a460d-124">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="a460d-124">Component\_</span></span>   |
|--------|---------------|
| <span data-ttu-id="a460d-125">миртле</span><span class="sxs-lookup"><span data-stu-id="a460d-125">Myrtle</span></span> | <span data-ttu-id="a460d-126">Миртле \_ пляже</span><span class="sxs-lookup"><span data-stu-id="a460d-126">Myrtle\_Beach</span></span> |



 

<span data-ttu-id="a460d-127">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a460d-127">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a460d-128">Компонент</span><span class="sxs-lookup"><span data-stu-id="a460d-128">Component</span></span>     | <span data-ttu-id="a460d-129">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="a460d-129">Directory\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="a460d-130">Миртле \_ пляже</span><span class="sxs-lookup"><span data-stu-id="a460d-130">Myrtle\_Beach</span></span> | <span data-ttu-id="a460d-131">сандбар</span><span class="sxs-lookup"><span data-stu-id="a460d-131">SandBar</span></span>     |



 

<span data-ttu-id="a460d-132">В этом примере шрифт Tahoma сопоставляется с файлом шрифта Миртле.</span><span class="sxs-lookup"><span data-stu-id="a460d-132">In this example, the font Tahoma maps to the font file Myrtle.</span></span> <span data-ttu-id="a460d-133">Файл Миртле принадлежит компоненту Миртле \_ пляже.</span><span class="sxs-lookup"><span data-stu-id="a460d-133">The file Myrtle belongs to the component Myrtle\_Beach.</span></span> <span data-ttu-id="a460d-134">Разрешение таблицы Directory показывает, что все файлы, принадлежащие Миртле \_ пляже, должны быть установлены в папку Сандбар.</span><span class="sxs-lookup"><span data-stu-id="a460d-134">Resolution of the Directory table shows that all the files belonging to Myrtle\_Beach are to be installed in the Sandbar folder.</span></span> <span data-ttu-id="a460d-135">Так как это не Фонтсфолдер, ICE07 отправляет сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a460d-135">Because this is not the FontsFolder, ICE07 posts an error message.</span></span>

<span data-ttu-id="a460d-136">Обратите внимание, что если компонент Миртле \_ пляже действительно принадлежит папке Сандбар, а не фонтсфолдер, то шрифт Tahoma может не входить в Миртле \_ пляже.</span><span class="sxs-lookup"><span data-stu-id="a460d-136">Note that if the component Myrtle\_Beach really belongs in the Sandbar folder, and not the FontsFolder, then the font Tahoma may not belong in Myrtle\_Beach.</span></span> <span data-ttu-id="a460d-137">Возможным исправлением ошибки является включение Tahoma в другой компонент, который устанавливается в каталог Фонтсфолдер.</span><span class="sxs-lookup"><span data-stu-id="a460d-137">A possible fix for the error would be to include Tahoma in another component that does get installed in the FontsFolder directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a460d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a460d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a460d-139">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="a460d-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



