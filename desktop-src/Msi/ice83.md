---
description: ICE83 проверяет таблицу Мсиассембли.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080675"
---
# <a name="ice83"></a><span data-ttu-id="87224-103">ICE83</span><span class="sxs-lookup"><span data-stu-id="87224-103">ICE83</span></span>

<span data-ttu-id="87224-104">ICE83 проверяет [таблицу мсиассембли](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="87224-104">ICE83 validates the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="87224-105">Это настраиваемое действие ICE отправляет ошибку, если путь к ключу для компонента, содержащего сборку Win32, установлен в файл манифеста.</span><span class="sxs-lookup"><span data-stu-id="87224-105">This ICE custom action posts an error if the key path for a component containing a Win32 assembly is set to the manifest file.</span></span> <span data-ttu-id="87224-106">Явная ошибка отправляется, если значение, указанное в поле ключевого пути [таблицы Component](component-table.md) , равно значению, указанному в \_ поле файл манифеста таблицы мсиассембли.</span><span class="sxs-lookup"><span data-stu-id="87224-106">Explicitly the error is posted if the value entered in the KeyPath field of the [Component table](component-table.md) equals the value entered in the File\_Manifest field of the MsiAssembly table.</span></span> <span data-ttu-id="87224-107">Это настраиваемое действие ICE отправляет ошибку, если в таблице Мсиассембли есть хотя бы одна запись, а [Таблица инсталлексекутесекуенце](installexecutesequence-table.md) не содержит как [действие мсипублишассемблиес](msipublishassemblies-action.md) , так и [действие мсиунпублишассемблиес](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="87224-107">This ICE custom action posts an error if there is at least one record in the MsiAssembly table and the [InstallExecuteSequence table](installexecutesequence-table.md) does not contain both the [MsiPublishAssemblies Action](msipublishassemblies-action.md) and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

## <a name="result"></a><span data-ttu-id="87224-108">Результат</span><span class="sxs-lookup"><span data-stu-id="87224-108">Result</span></span>

<span data-ttu-id="87224-109">ICE83 отправляет следующие ошибки.</span><span class="sxs-lookup"><span data-stu-id="87224-109">ICE83 posts the following errors.</span></span>



| <span data-ttu-id="87224-110">ICE83, ошибка</span><span class="sxs-lookup"><span data-stu-id="87224-110">ICE83 error</span></span>                                                                                                   | <span data-ttu-id="87224-111">Описание</span><span class="sxs-lookup"><span data-stu-id="87224-111">Description</span></span>                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87224-112">Путь к ключу для сборки Win32 SxS (компонент \_ = \[ 1 \] ) не должен быть файлом манифеста</span><span class="sxs-lookup"><span data-stu-id="87224-112">The key path for Win32 SXS Assembly (Component\_=\[1\]) SHOULD NOT be its manifest file</span></span>                       | <span data-ttu-id="87224-113">ICE83 отправляет эту ошибку, если поле ключевого пути для сборки Win32 имеет значение файла манифеста (Component. ключевой = = Мсиассембли. file \_ manifest).</span><span class="sxs-lookup"><span data-stu-id="87224-113">ICE83 posts this error when the KeyPath field for a Win32 Assembly is set to its manifest file (Component.KeyPath == MsiAssembly.File\_Manifest).</span></span> <span data-ttu-id="87224-114">\[1 \] — ключевой путь в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="87224-114">\[1\] is KeyPath in Component table</span></span>                          |
| <span data-ttu-id="87224-115">В таблице Инсталлексекутесекуенце должны присутствовать действия Мсипублишассемблиес и Мсиунпублишассемблиес.</span><span class="sxs-lookup"><span data-stu-id="87224-115">Both MsiPublishAssemblies AND MsiUnpublishAssemblies actions MUST be present in InstallExecuteSequence table.</span></span> | <span data-ttu-id="87224-116">ICE83 отправляет эту ошибку, если в таблице Мсиассембли есть хотя бы одна запись, но таблица Инсталлексекутесекуенце не содержит как действие Мсиассемблипублиш, так и действие Мсиассемблюнпублиш.</span><span class="sxs-lookup"><span data-stu-id="87224-116">ICE83 posts this error when there is at least one entry in the MsiAssembly table but the InstallExecuteSequence table does not contain both the MsiAssemblyPublish action and the MsiAssemblyUnpublish action.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="87224-117">См. также</span><span class="sxs-lookup"><span data-stu-id="87224-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87224-118">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="87224-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



