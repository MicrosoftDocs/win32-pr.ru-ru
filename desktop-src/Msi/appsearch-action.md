---
description: Действие Аппсеарч использует подписи файлов для поиска существующих версий продуктов.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Действие Аппсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264197"
---
# <a name="appsearch-action"></a><span data-ttu-id="53192-103">Действие Аппсеарч</span><span class="sxs-lookup"><span data-stu-id="53192-103">AppSearch Action</span></span>

<span data-ttu-id="53192-104">Действие Аппсеарч использует подписи файлов для поиска существующих версий продуктов.</span><span class="sxs-lookup"><span data-stu-id="53192-104">The AppSearch action uses file signatures to search for existing versions of products.</span></span> <span data-ttu-id="53192-105">Действие Аппсеарч может использовать эти сведения для определения места установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="53192-105">The AppSearch action may use this information to determine where upgrades are to be installed.</span></span> <span data-ttu-id="53192-106">Действие Аппсеарч также можно использовать для задания свойству существующего значения записи реестра или INI-файла.</span><span class="sxs-lookup"><span data-stu-id="53192-106">The AppSearch action can also be used to set a property to the existing value of an registry or .ini file entry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="53192-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="53192-107">Sequence Restrictions</span></span>

<span data-ttu-id="53192-108">Аппсеарч должен быть создан в [таблице инсталлуисекуенце](installuisequence-table.md) и [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="53192-108">AppSearch should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="53192-109">Установщик предотвращает выполнение действия Аппсеарч в последовательности Инсталлексекутесекуенце, если действие уже выполнялось в последовательности Инсталлуисекуенце.</span><span class="sxs-lookup"><span data-stu-id="53192-109">The installer prevents the AppSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="53192-110">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="53192-110">ActionData Messages</span></span>



| <span data-ttu-id="53192-111">Поле</span><span class="sxs-lookup"><span data-stu-id="53192-111">Field</span></span> | <span data-ttu-id="53192-112">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="53192-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="53192-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="53192-113">\[1\]</span></span> | <span data-ttu-id="53192-114">Свойство, содержащее расположение файла.</span><span class="sxs-lookup"><span data-stu-id="53192-114">Property holding file location.</span></span> |
| <span data-ttu-id="53192-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="53192-115">\[2\]</span></span> | <span data-ttu-id="53192-116">Подпись файла.</span><span class="sxs-lookup"><span data-stu-id="53192-116">File signature.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="53192-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53192-117">Remarks</span></span>

<span data-ttu-id="53192-118">Для действия Аппсеарч требуется, чтобы таблица [сигнатур](signature-table.md) присутствовала в установочном пакете.</span><span class="sxs-lookup"><span data-stu-id="53192-118">The AppSearch action requires that the [Signature](signature-table.md) table be present in the installation package.</span></span> <span data-ttu-id="53192-119">Подписи файлов перечислены в таблице сигнатур.</span><span class="sxs-lookup"><span data-stu-id="53192-119">File signatures are listed in the Signature table.</span></span> <span data-ttu-id="53192-120">Подпись, не указанная в таблице сигнатур, обозначает каталог, а действие задает для свойства путь к каталогу для этой сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="53192-120">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="53192-121">Действие Аппсеарч ищет подписи файлов сначала с помощью таблицы [комплокатор](complocator-table.md) , а затем таблицу [реглокатор](reglocator-table.md) , затем таблицу [инилокатор](inilocator-table.md) и, наконец, таблицу [дрлокатор](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="53192-121">The AppSearch action searches for file signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table next, then the [IniLocator](inilocator-table.md) table, and finally the [DrLocator](drlocator-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53192-122">См. также</span><span class="sxs-lookup"><span data-stu-id="53192-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53192-123">аппсеарч</span><span class="sxs-lookup"><span data-stu-id="53192-123">AppSearch</span></span>](appsearch-table.md)
</dt> <dt>

[<span data-ttu-id="53192-124">комплокатор</span><span class="sxs-lookup"><span data-stu-id="53192-124">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="53192-125">инилокатор</span><span class="sxs-lookup"><span data-stu-id="53192-125">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="53192-126">реглокатор</span><span class="sxs-lookup"><span data-stu-id="53192-126">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="53192-127">дрлокатор</span><span class="sxs-lookup"><span data-stu-id="53192-127">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



