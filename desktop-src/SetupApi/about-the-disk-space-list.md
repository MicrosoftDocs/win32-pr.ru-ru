---
description: Список дискового пространства позволяет вычислить место на диске, необходимое для завершения операций установки.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: О списке Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662339"
---
# <a name="about-the-disk-space-list"></a><span data-ttu-id="81486-103">О списке Disk-Space</span><span class="sxs-lookup"><span data-stu-id="81486-103">About the Disk-Space List</span></span>

<span data-ttu-id="81486-104">Список дискового пространства позволяет вычислить место на диске, необходимое для завершения операций установки.</span><span class="sxs-lookup"><span data-stu-id="81486-104">The disk-space list enables you to calculate the disk space required to complete the installation operations.</span></span> <span data-ttu-id="81486-105">После создания списка дискового пространства и добавления в него файловых операций можно запросить список, чтобы определить целевые диски, указанные в операциях с файлами, и место на диске, необходимое для каждого диска.</span><span class="sxs-lookup"><span data-stu-id="81486-105">After you create a disk-space list and add file operations to it, you can query the list to determine the target drives specified by the file operations, and the disk space required on each drive.</span></span>

<span data-ttu-id="81486-106">Сравнивая пространство, необходимое для свободного места на целевых дисках, можно программным образом определить, достаточно ли свободного места для текущей установки.</span><span class="sxs-lookup"><span data-stu-id="81486-106">By comparing the space required to the space available on the target disks, you can programmatically determine whether sufficient space is available for the current installation.</span></span>

<span data-ttu-id="81486-107">Вы можете добавить или удалить файловые операции в списке дискового пространства и повторно рассчитать необходимый объем дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="81486-107">You can add or remove file operations to the disk-space list and recalculate the disk space required.</span></span> <span data-ttu-id="81486-108">Эта функция позволяет, например, написать программу, которая взаимодействует с пользователем, позволяя ему выбрать компоненты, которые требуется установить, в зависимости от требуемого места на диске.</span><span class="sxs-lookup"><span data-stu-id="81486-108">This functionality enables you to, for example, write a program that interacts with the user, allowing him or her to choose what components they want to install based on the disk space required.</span></span>

<span data-ttu-id="81486-109">Функции списка дискового пространства автоматически проверяют наличие существующих копий файлов на целевом диске.</span><span class="sxs-lookup"><span data-stu-id="81486-109">The disk-space list functions automatically check for preexisting copies of files on the target disk.</span></span> <span data-ttu-id="81486-110">Если была найдена Предыдущая версия файла, функции списка дискового пространства вычисляют дополнительное пространство, необходимое для завершения операций с файлами.</span><span class="sxs-lookup"><span data-stu-id="81486-110">If a previous version of the file is found, the disk-space list functions calculate the additional space required to complete the file operations.</span></span>

<span data-ttu-id="81486-111">Например, если операция копирования указывает, что 6000-байтовый файл будет скопирован на диск C, а на диске C уже существует 2000-байтовый файл, то функции дискового пространства будут возвращать требуемый объем в 4000 байт.</span><span class="sxs-lookup"><span data-stu-id="81486-111">For example, if a copy operation specifies that a 6000-byte file be copied to drive C, and a 2000-byte version of that file already exists on the drive C, the disk space functions would return a required space of 4000 bytes.</span></span> <span data-ttu-id="81486-112">Дополнительное пространство используется для замены более старой версии файла новой версией.</span><span class="sxs-lookup"><span data-stu-id="81486-112">The additional space is used to replace the older version of the file with the newer version.</span></span>

<span data-ttu-id="81486-113">В списке дискового пространства функции округляют размер файлов в границах кластерных дисков.</span><span class="sxs-lookup"><span data-stu-id="81486-113">The disk-space list functions round file sizes to the disk cluster boundaries.</span></span>

 

 



