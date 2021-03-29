---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810390"
---
# <a name="d-windows-installer"></a><span data-ttu-id="f9225-103">D (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="f9225-103">D (Windows Installer)</span></span>

<span data-ttu-id="f9225-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="f9225-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f9225-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**Функция базы данных**</span><span class="sxs-lookup"><span data-stu-id="f9225-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="f9225-106">Обращается к базе данных установщика.</span><span class="sxs-lookup"><span data-stu-id="f9225-106">Accesses the installer database.</span></span> <span data-ttu-id="f9225-107">Эти функции предоставляются главным образом для использования [*средствами разработки пакетов установщика*](i-gly.md) , и они не предназначены для использования при вызове служб установщика.</span><span class="sxs-lookup"><span data-stu-id="f9225-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="f9225-108">Дополнительные сведения см. в разделе [функции базы данных](database-functions.md) и [Справочник по функциям установщика](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f9225-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9225-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**маркер базы данных**</span><span class="sxs-lookup"><span data-stu-id="f9225-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="f9225-110">Требуется для работы с базой данных.</span><span class="sxs-lookup"><span data-stu-id="f9225-110">Required for working with a database.</span></span> <span data-ttu-id="f9225-111">Дополнительные сведения см. [в разделе Получение маркера базы данных](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="f9225-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9225-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**Дельта исправления**</span><span class="sxs-lookup"><span data-stu-id="f9225-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="f9225-113">Разностное обновление — это установщик Windows исправление с разностным сжатием, созданное с помощью средства, такого как Patchwiz.dll, которое поддерживает разностное сжатие.</span><span class="sxs-lookup"><span data-stu-id="f9225-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="f9225-114">Исправления, использующие разностное сжатие, могут уменьшить размер обновления, предоставляя только различия (разности) между существующими файлами на целевом компьютере и новыми файлами.</span><span class="sxs-lookup"><span data-stu-id="f9225-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="f9225-115">Затем нужные новые файлы будут синтезированы на основе существующих файлов и загруженных дельты.</span><span class="sxs-lookup"><span data-stu-id="f9225-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="f9225-116">Дополнительные сведения о технологии разностного сжатия см. в разделе [интерфейс программирования приложений для разностного сжатия](https://msdn.microsoft.com/library/ms811406.aspx).</span><span class="sxs-lookup"><span data-stu-id="f9225-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



