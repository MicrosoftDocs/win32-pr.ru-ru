---
description: Каждый файл и каталог на томе, который поддерживает сжатие для отдельных файлов и каталогов, имеет состояние сжатия.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Состояние сжатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264730"
---
# <a name="compression-state"></a><span data-ttu-id="410b4-103">Состояние сжатия</span><span class="sxs-lookup"><span data-stu-id="410b4-103">Compression State</span></span>

<span data-ttu-id="410b4-104">Каждый файл и каталог на томе, который поддерживает сжатие для отдельных файлов и каталогов, имеет *состояние сжатия*.</span><span class="sxs-lookup"><span data-stu-id="410b4-104">Each file and directory on a volume that supports compression for individual files and directories has a *compression state*.</span></span>

<span data-ttu-id="410b4-105">В то время как атрибут сжатия файла или каталога указывает на то, что файл или каталог сжат или не сжат, в состоянии сжатия также указывается формат любых сжатых данных.</span><span class="sxs-lookup"><span data-stu-id="410b4-105">Whereas the compression attribute of a file or directory indicates simply whether the file or directory is compressed or not compressed, the compression state also specifies the format of any compressed data.</span></span>

<span data-ttu-id="410b4-106">Используйте управляющий код [**\_ получения \_ сжатия фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) , чтобы определить состояние сжатия файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="410b4-106">Use the [**FSCTL\_GET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) control code to determine the compression state of a file or directory.</span></span>

<span data-ttu-id="410b4-107">Состояние сжатия кодируется как 16-разрядное значение.</span><span class="sxs-lookup"><span data-stu-id="410b4-107">Compression state is encoded as a 16-bit value.</span></span> <span data-ttu-id="410b4-108">Значение состояния сжатия в формате СЖАТИЯ \_ \_ None означает, что файл не сжат.</span><span class="sxs-lookup"><span data-stu-id="410b4-108">A compression state value of COMPRESSION\_FORMAT\_NONE indicates that a file is not compressed.</span></span> <span data-ttu-id="410b4-109">Значение \_ формата сжатия \_ Default указывает, что файл сжимается с использованием формата сжатия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="410b4-109">A value of COMPRESSION\_FORMAT\_DEFAULT indicates that a file is compressed, using the default compression format.</span></span> <span data-ttu-id="410b4-110">Любое другое значение указывает на то, что файл сжат, используя формат сжатия, заданный значением состояния сжатия.</span><span class="sxs-lookup"><span data-stu-id="410b4-110">Any other value indicates that a file is compressed, using the compression format specified by the compression state value.</span></span>

<span data-ttu-id="410b4-111">Для задания состояния сжатия файла или каталога используйте управляющий код [**фсктл \_ Set \_ Compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .</span><span class="sxs-lookup"><span data-stu-id="410b4-111">Use the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code to set the compression state of a file or directory.</span></span> <span data-ttu-id="410b4-112">Эта операция также задает атрибут сжатия файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="410b4-112">This operation also sets the compression attribute of the file or directory.</span></span>

<span data-ttu-id="410b4-113">При установке состояния сжатия файла в ненулевое значение сжимается файл с использованием формата сжатия, закодированного значением состояния сжатия.</span><span class="sxs-lookup"><span data-stu-id="410b4-113">Setting the compression state of a file to a nonzero value compresses the file, using the compression format encoded by the compression state value.</span></span> <span data-ttu-id="410b4-114">При установке для файла состояния сжатия значение нуль распаковывает файл.</span><span class="sxs-lookup"><span data-stu-id="410b4-114">Setting a file's compression state to zero decompresses the file.</span></span> <span data-ttu-id="410b4-115">Это синхронные операции.</span><span class="sxs-lookup"><span data-stu-id="410b4-115">These are synchronous operations.</span></span> <span data-ttu-id="410b4-116">Файл сжимается или распаковывается сразу же после установки состояния сжатия.</span><span class="sxs-lookup"><span data-stu-id="410b4-116">The file is compressed or decompressed immediately when you set its compression state.</span></span>

<span data-ttu-id="410b4-117">Настройка состояния сжатия каталога не приводит к немедленному сжатию или распаковке.</span><span class="sxs-lookup"><span data-stu-id="410b4-117">Setting a directory's compression state does not cause any immediate compression or decompression.</span></span> <span data-ttu-id="410b4-118">Вместо этого при настройке состояния сжатия каталога устанавливается состояние сжатия по умолчанию, которое будет предоставлено всем вновь созданным файлам и подкаталогам.</span><span class="sxs-lookup"><span data-stu-id="410b4-118">Instead, setting a directory's compression state sets a default compression state that will be given to all newly created files and subdirectories.</span></span>

 

 
