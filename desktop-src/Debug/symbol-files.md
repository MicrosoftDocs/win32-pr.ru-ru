---
description: Как правило, отладочная информация хранится в файле символов, отдельном от исполняемого файла.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Файлы символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141022"
---
# <a name="symbol-files"></a><span data-ttu-id="10cf4-103">Файлы символов</span><span class="sxs-lookup"><span data-stu-id="10cf4-103">Symbol Files</span></span>

<span data-ttu-id="10cf4-104">Как правило, отладочная информация хранится в файле символов, отдельном от исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="10cf4-104">Normally, debugging information is stored in a symbol file separate from the executable.</span></span> <span data-ttu-id="10cf4-105">Реализация этой отладочной информации была изменена в течение нескольких лет, и в следующей документации будет предоставлено руководство по различным реализациям.</span><span class="sxs-lookup"><span data-stu-id="10cf4-105">The implementation of this debugging information has changed over the years, and the following documentation will provide guidance regarding these various implementations.</span></span>

## <a name="pdb-files"></a><span data-ttu-id="10cf4-106">PDB-файлы</span><span class="sxs-lookup"><span data-stu-id="10cf4-106">PDB files</span></span>

<span data-ttu-id="10cf4-107">Все современные версии компиляторов Майкрософт хранят сведения об отладке скомпилированного исполняемого файла в отдельном файле *базы данных программы* (. pdb).</span><span class="sxs-lookup"><span data-stu-id="10cf4-107">All modern versions of the Microsoft compilers store debugging information about a compiled executable in a separate *program database* (.pdb) file.</span></span> <span data-ttu-id="10cf4-108">Этот файл обычно называют *pdb*-файлом.</span><span class="sxs-lookup"><span data-stu-id="10cf4-108">This file is commonly referred to as a *PDB*.</span></span> <span data-ttu-id="10cf4-109">Данные хранятся в отдельном файле из исполняемого файла, что позволяет ограничить размер исполняемого файла, экономя дискового пространства и сокращая время, затрачиваемое на загрузку данных.</span><span class="sxs-lookup"><span data-stu-id="10cf4-109">The data is stored in a separate file from the executable to help limit the size of the executable, saving disk storage space and reducing the time it takes to load the data.</span></span> <span data-ttu-id="10cf4-110">Эта методика также позволяет распределять исполняемый файл без закрытия этих существенных сведений, что может сделать программу более удобной для реконструирования.</span><span class="sxs-lookup"><span data-stu-id="10cf4-110">This methodology also allows the executable to be distributed without disclosing this significant information which could make the program easier to reverse engineer.</span></span>

<span data-ttu-id="10cf4-111">Чтобы создать PDB, создайте исполняемый файл с отладочной информацией в соответствии с инструкциями для средств сборки.</span><span class="sxs-lookup"><span data-stu-id="10cf4-111">To create a PDB, build your executable file with debugging information according to the directions for your build tools.</span></span>

<span data-ttu-id="10cf4-112">API DbgHelp может использовать PDB для получения следующих сведений.</span><span class="sxs-lookup"><span data-stu-id="10cf4-112">The DbgHelp API is able to use PDBs to obtain the following information.</span></span>

-   <span data-ttu-id="10cf4-113">общедоступные и экспортные</span><span class="sxs-lookup"><span data-stu-id="10cf4-113">publics and exports</span></span>
-   <span data-ttu-id="10cf4-114">глобальные символы</span><span class="sxs-lookup"><span data-stu-id="10cf4-114">global symbols</span></span>
-   <span data-ttu-id="10cf4-115">локальные символы</span><span class="sxs-lookup"><span data-stu-id="10cf4-115">local symbols</span></span>
-   <span data-ttu-id="10cf4-116">данные типа</span><span class="sxs-lookup"><span data-stu-id="10cf4-116">type data</span></span>
-   <span data-ttu-id="10cf4-117">исходные файлы</span><span class="sxs-lookup"><span data-stu-id="10cf4-117">source files</span></span>
-   <span data-ttu-id="10cf4-118">номера строк</span><span class="sxs-lookup"><span data-stu-id="10cf4-118">line numbers</span></span>

## <a name="dbg-files-and-embedded-debug-information"></a><span data-ttu-id="10cf4-119">DBG файлы и внедренная отладочная информация</span><span class="sxs-lookup"><span data-stu-id="10cf4-119">DBG files and embedded debug information</span></span>

<span data-ttu-id="10cf4-120">Предыдущие версии набора инструментов Microsoft использовались для внедрения отладочной информации в исполняемый файл, но обычно они были удалены в отдельный файл с расширением. dbg.</span><span class="sxs-lookup"><span data-stu-id="10cf4-120">Previous versions of the Microsoft toolset used to embed the debugging information in the executable, however it would normally be stripped out into a separate file with a .dbg extension.</span></span> <span data-ttu-id="10cf4-121">Этот файл обычно называют *dbg* -файлом.</span><span class="sxs-lookup"><span data-stu-id="10cf4-121">This is commonly known as a *DBG* file.</span></span> <span data-ttu-id="10cf4-122">Файлы DBG используют один и тот же формат PE в качестве исполняемых файлов.</span><span class="sxs-lookup"><span data-stu-id="10cf4-122">DBG files use the same PE file format as executables.</span></span>

<span data-ttu-id="10cf4-123">Поддержка API DbgHelp для Дбгс и встроенной отладочной информации ограничена и включает следующее.</span><span class="sxs-lookup"><span data-stu-id="10cf4-123">The DbgHelp API support for DBGs and embedded debugging information is limited and includes the following.</span></span>

-   <span data-ttu-id="10cf4-124">общедоступные и экспортные</span><span class="sxs-lookup"><span data-stu-id="10cf4-124">publics and exports</span></span>
-   <span data-ttu-id="10cf4-125">глобальные символы</span><span class="sxs-lookup"><span data-stu-id="10cf4-125">global symbols</span></span>

 

 



