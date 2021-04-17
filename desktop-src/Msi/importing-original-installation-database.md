---
description: Начните разработку пакета обновления, скопировав установочный пакет и дерево исходного каталога исходного продукта.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Импорт исходной базы данных установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650967"
---
# <a name="importing-original-installation-database"></a><span data-ttu-id="9d353-103">Импорт исходной базы данных установки</span><span class="sxs-lookup"><span data-stu-id="9d353-103">Importing Original Installation Database</span></span>

<span data-ttu-id="9d353-104">Начните разработку пакета обновления, скопировав установочный пакет и дерево исходного каталога исходного продукта.</span><span class="sxs-lookup"><span data-stu-id="9d353-104">Begin authoring the upgrade package by copying the installation package and source directory tree of the of original product.</span></span> <span data-ttu-id="9d353-105">Инструкции по созданию пакета установки для MNP2000 приведены в [примере установки](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="9d353-105">Instructions for authoring the installation package for MNP2000 are given in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="9d353-106">Необходимо скопировать содержимое следующих папок:</span><span class="sxs-lookup"><span data-stu-id="9d353-106">You should copy the contents of the following folders:</span></span>

<span data-ttu-id="9d353-107">В. \\ пример \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="9d353-107">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="9d353-108">В. \\ пример \\ блокнота</span><span class="sxs-lookup"><span data-stu-id="9d353-108">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="9d353-109">В. \\ пример \\ двоичного файла</span><span class="sxs-lookup"><span data-stu-id="9d353-109">C:\\Sample\\Binary</span></span>\\

<span data-ttu-id="9d353-110">C: \\ \\ значок образца</span><span class="sxs-lookup"><span data-stu-id="9d353-110">C:\\Sample\\Icon</span></span>\\

<span data-ttu-id="9d353-111">Обновите содержимое папки блокнота, чтобы они соответствовали источнику, описанному в разделе [планирование основного обновления](planning-a-major-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="9d353-111">Update the contents of the Notepad folder so that they match the source described in [Planning a Major Upgrade](planning-a-major-upgrade.md).</span></span> <span data-ttu-id="9d353-112">Удалите все устаревшие исходные файлы, например Baseball.txt, и замените их обновленными файлами, такими как Baseba01.txt.</span><span class="sxs-lookup"><span data-stu-id="9d353-112">Remove all obsolete source files, such as Baseball.txt, and replace with the updated files, such as Baseba01.txt.</span></span> <span data-ttu-id="9d353-113">Добавьте дополнительные новые файлы, предоставляемые обновлением, например Opera01.txt.</span><span class="sxs-lookup"><span data-stu-id="9d353-113">Add the additional new files provided by the upgrade, such as Opera01.txt.</span></span>

<span data-ttu-id="9d353-114">Переименуйте MNP2000.msi в MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="9d353-114">Rename MNP2000.msi to MNP2001.msi.</span></span> <span data-ttu-id="9d353-115">В последующих шагах будет использоваться редактор таблиц для изменения этой базы данных в MSI-файл для обновления.</span><span class="sxs-lookup"><span data-stu-id="9d353-115">In subsequent steps you will use a table editor to modify this database into the .msi file for the upgrade.</span></span> <span data-ttu-id="9d353-116">Таблицы базы данных, которые не были явно изменены в последующих разделах, идентичны таблицам в базе данных исходного продукта MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="9d353-116">Database tables that are not explicitly modified in the subsequent sections are identical to the tables in the original product's database, MNP2000.msi.</span></span>

[<span data-ttu-id="9d353-117">Продолжить</span><span class="sxs-lookup"><span data-stu-id="9d353-117">Continue</span></span>](updating-directory-structure-for-an-upgrade.md)

 

 



