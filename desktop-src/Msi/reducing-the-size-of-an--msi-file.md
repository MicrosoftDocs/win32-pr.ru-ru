---
description: Разработчики установщик Windowsных пакетов могут заметить, что файлы MSI получают больший размер, чем ожидалось после повторного редактирования и сохранения.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Уменьшение размера MSI файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998419"
---
# <a name="reducing-the-size-of-an-msi-file"></a><span data-ttu-id="faa9c-103">Уменьшение размера MSI файла</span><span class="sxs-lookup"><span data-stu-id="faa9c-103">Reducing the Size of an .msi File</span></span>

<span data-ttu-id="faa9c-104">Разработчики установщик Windowsных пакетов могут заметить, что файлы MSI получают больший размер, чем ожидалось после повторного редактирования и сохранения.</span><span class="sxs-lookup"><span data-stu-id="faa9c-104">Developers of Windows Installer packages may notice their .msi files getting larger than expected after repeated edits and saves.</span></span> <span data-ttu-id="faa9c-105">Установщик Windows файлы MSI являются составными файлами, содержащими хранилища и потоки, и имеют некоторые из тех же ограничений хранилища, что и файлы документов OLE.</span><span class="sxs-lookup"><span data-stu-id="faa9c-105">Windows Installer .msi files are compound files that contain storages and streams, and have some of the same storage limitations as OLE document files.</span></span> <span data-ttu-id="faa9c-106">Если изменить и сохранить один и тот же MSI-файл поверх и снова, он создаст неиспользуемое дисковое пространство в файле.</span><span class="sxs-lookup"><span data-stu-id="faa9c-106">If you edit and save the same .msi file over and over, it creates wasted storage space in the file.</span></span> <span data-ttu-id="faa9c-107">Это касается только авторов MSI файлов и не влияет на установщик Windows пользователей.</span><span class="sxs-lookup"><span data-stu-id="faa9c-107">This only affects authors of .msi files and has no effect on Windows Installer users.</span></span> <span data-ttu-id="faa9c-108">Разработчикам может потребоваться удалить это неиспользуемое дисковое пространство перед отправкой конечного MSI-файла.</span><span class="sxs-lookup"><span data-stu-id="faa9c-108">Developers may want to remove this wasted storage space before shipping their final .msi file.</span></span>

<span data-ttu-id="faa9c-109">Чтобы удалить неиспользуемое дисковое пространство и сократить окончательный размер MSI-файлов, можно использовать следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="faa9c-109">To remove wasted storage space and reduce the final size of .msi files, you have the following options.</span></span>

-   <span data-ttu-id="faa9c-110">Экспортируйте все таблицы в базе данных в файлы IDT, а затем импортируйте их в новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="faa9c-110">Export all of the tables in the database to .idt files, and then import those into a new database.</span></span> <span data-ttu-id="faa9c-111">Это позволяет получить максимально компактное хранилище.</span><span class="sxs-lookup"><span data-stu-id="faa9c-111">This produces the most compact storage possible.</span></span>
-   <span data-ttu-id="faa9c-112">Использование служебной программы для сжатия пространства хранения файлов документов OLE.</span><span class="sxs-lookup"><span data-stu-id="faa9c-112">Use a software utility for compacting the storage space of OLE document files.</span></span>

 

 



