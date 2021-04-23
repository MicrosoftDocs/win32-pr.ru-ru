---
description: ICE18 проверяет, что все пустые каталоги, используемые в качестве пути к ключу для компонента, перечислены в таблице Креатефолдер.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662579"
---
# <a name="ice18"></a><span data-ttu-id="a28d3-103">ICE18</span><span class="sxs-lookup"><span data-stu-id="a28d3-103">ICE18</span></span>

<span data-ttu-id="a28d3-104">ICE18 проверяет, что все пустые каталоги, используемые в качестве пути к ключу для компонента, перечислены в [таблице креатефолдер](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="a28d3-104">ICE18 validates that any empty directories used as a key path for a component are listed in the [CreateFolder table](createfolder-table.md).</span></span>

<span data-ttu-id="a28d3-105">Если столбец ключевого пути в [таблице Component](component-table.md) имеет значение null, это означает, что каталог, указанный в столбце Directory, \_ является ключевым путем для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="a28d3-105">If the KeyPath column of the [Component table](component-table.md) is Null, this means that directory listed in the Directory\_ column is the key path for that component.</span></span> <span data-ttu-id="a28d3-106">Поскольку папки, созданные установщиком, удаляются, когда они становятся пустыми, эта папка должна быть указана в [таблице креатефолдер](createfolder-table.md) , чтобы установщик не пытался установить каждый раз.</span><span class="sxs-lookup"><span data-stu-id="a28d3-106">Because folders created by the installer are deleted when they become empty, this folder must be listed in the [CreateFolder table](createfolder-table.md) to prevent the installer from attempting to install every time.</span></span>

<span data-ttu-id="a28d3-107">Не следует делать каталог Системфолдер ключевым путем к компоненту.</span><span class="sxs-lookup"><span data-stu-id="a28d3-107">Do not make the SystemFolder directory the key path of a component.</span></span> <span data-ttu-id="a28d3-108">Так как эта папка имеется в каждой операционной системе, установщик всегда определяет путь к ключу независимо от наличия компонента.</span><span class="sxs-lookup"><span data-stu-id="a28d3-108">Because this folder is present on every operating system, the installer always detects the key path whether or not the component is present.</span></span> <span data-ttu-id="a28d3-109">В этом случае путь к ключу должен быть файлом, записью реестра или источником данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="a28d3-109">In this case, the key path should be a file, registry entry, or ODBC data source.</span></span>

<span data-ttu-id="a28d3-110">При выполнении проверки ICE18 сначала проверяет, выполняются ли следующие условия:</span><span class="sxs-lookup"><span data-stu-id="a28d3-110">When performing a validation ICE18 first checks whether the following are all true:</span></span>

-   <span data-ttu-id="a28d3-111">Ключевой столбец [таблицы Component](component-table.md) содержит значение null.</span><span class="sxs-lookup"><span data-stu-id="a28d3-111">The KeyPath column of the [Component table](component-table.md) contains a Null value.</span></span>
-   <span data-ttu-id="a28d3-112">В [таблице File](file-table.md)нет файлов, перечисленных для компонента.</span><span class="sxs-lookup"><span data-stu-id="a28d3-112">That there are no files listed for the component in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="a28d3-113">Отсутствие файлов для компонента, указанного в [таблице ремовефиле](removefile-table.md) , и то, что значение в дирпроперти совпадает со \_ столбцом Directory [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a28d3-113">That there are no files for the component listed in the [RemoveFile table](removefile-table.md) and that the value in the DirProperty is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="a28d3-114">Отсутствие файлов для компонента, указанного в [таблице дупликатефиле](duplicatefile-table.md) , и то, что значение в DestFolder совпадает со \_ столбцом Directory [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a28d3-114">That there are no files for the component listed in the [DuplicateFile table](duplicatefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="a28d3-115">Отсутствие файлов для компонента, указанного в [таблице MoveFile](movefile-table.md) , и то, что значение в DestFolder совпадает со \_ столбцом Directory [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a28d3-115">That there are no files for the component listed in the [MoveFile table](movefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="a28d3-116">Если все это верно, ICE18 проверяет следующее:</span><span class="sxs-lookup"><span data-stu-id="a28d3-116">If these are all true then ICE18 validates the following:</span></span>

-   <span data-ttu-id="a28d3-117">\_Столбец Component [таблицы креатефолдер](createfolder-table.md) имеет то же значение, что и столбец Component [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a28d3-117">That the Component\_ column of the [CreateFolder table](createfolder-table.md) has the same value as the Component column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="a28d3-118">\_Столбец Directory таблицы креатефолдер имеет то же значение, что и \_ столбец Directory [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a28d3-118">That the Directory\_ column of the CreateFolder table has the same value as the Directory\_ column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="a28d3-119">Результат</span><span class="sxs-lookup"><span data-stu-id="a28d3-119">Result</span></span>

<span data-ttu-id="a28d3-120">ICE18 отправляет сообщение об ошибке, если установочный пакет указывает каталог в качестве пути к разделу для компонента, который не указан в [таблице креатефолдер](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="a28d3-120">ICE18 posts an error message if the installation package specifies a directory as the key path for component that is not listed in the [CreateFolder table](createfolder-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a28d3-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a28d3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a28d3-122">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="a28d3-122">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



