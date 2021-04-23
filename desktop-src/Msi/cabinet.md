---
description: Тип данных CAB должен использоваться в столбце CAB-файла таблицы Media.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: Файле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909040"
---
# <a name="cabinet"></a><span data-ttu-id="d302e-103">Файле</span><span class="sxs-lookup"><span data-stu-id="d302e-103">Cabinet</span></span>

<span data-ttu-id="d302e-104">Тип данных CAB должен использоваться в столбце CAB-файла [таблицы Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="d302e-104">The Cabinet data type must be used in the Cabinet column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="d302e-105">Если перед именем CAB-файла стоит знак решетки, CAB-файл сохраняется в виде потока данных внутри пакета.</span><span class="sxs-lookup"><span data-stu-id="d302e-105">If the cabinet name is preceded by the number sign, the cabinet is stored as a data stream inside the package.</span></span> <span data-ttu-id="d302e-106">Строка символов, следующая за, \# является [идентификатором](identifier.md) для этого потока данных.</span><span class="sxs-lookup"><span data-stu-id="d302e-106">The character string which follows the \# is an [Identifier](identifier.md) for this data stream.</span></span> <span data-ttu-id="d302e-107">Обратите внимание, что если CAB-файл хранится в виде потока данных, в имени ящика учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="d302e-107">Note that if the cabinet is stored as a data stream, the name of a cabinet is case-sensitive.</span></span>

<span data-ttu-id="d302e-108">Если перед именем CAB-файла не стоит знак решетки \# , CAB-файл хранится в отдельном файле, расположенном в корне исходного дерева, заданном в [таблице Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="d302e-108">If the cabinet name is not preceded by the number sign \#, the cabinet is stored in a separate file located at the root of the source tree specified by the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="d302e-109">CAB-файл должен использовать короткий синтаксис имени файла, состоящий из восьми символов, точек и трех расширений символов.</span><span class="sxs-lookup"><span data-stu-id="d302e-109">The cabinet file must use the short file name syntax consisting of an eight character name, a period, and a three character extension.</span></span> <span data-ttu-id="d302e-110">Тип данных CAB-файла не может использовать короткий \| синтаксис LongName для имен файлов.</span><span class="sxs-lookup"><span data-stu-id="d302e-110">The Cabinet data type cannot use the short\|longname syntax for file names.</span></span> <span data-ttu-id="d302e-111">Если CAB-файл хранится в отдельном файле, то имя файла CAB не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d302e-111">If the cabinet file is stored as a separate file, the name of the cabinet file is not case-sensitive.</span></span>

<span data-ttu-id="d302e-112">Чтобы сэкономить место на диске, установщик удаляет все ящики, внедренные в MSI-файл, перед кэшированием пакета установки на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="d302e-112">To conserve disk space, the installer removes any cabinets embedded in the .msi file before caching the installation package on the user's computer.</span></span>

<span data-ttu-id="d302e-113">См. раздел [Включение CAB-файла в установку](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="d302e-113">See [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



