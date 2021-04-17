---
description: Тип данных Дефаултдир — это текстовая строка, содержащая либо допустимое имя файла, либо допустимый идентификатор.
ms.assetid: c7c5eac1-3283-4878-9d0d-887f93fc7a35
title: дефаултдир
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 957c826ec2b0850710d761def2f758691f923d9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663715"
---
# <a name="defaultdir"></a><span data-ttu-id="28b69-103">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="28b69-103">DefaultDir</span></span>

<span data-ttu-id="28b69-104">Тип данных Дефаултдир — это текстовая строка, содержащая либо допустимое [имя файла](filename.md) , либо допустимый [идентификатор](identifier.md).</span><span class="sxs-lookup"><span data-stu-id="28b69-104">The DefaultDir data type is a text string containing either a valid [Filename](filename.md) or a valid [Identifier](identifier.md).</span></span> <span data-ttu-id="28b69-105">Он используется только в [таблице Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="28b69-105">This is used only in the [Directory table](directory-table.md).</span></span> <span data-ttu-id="28b69-106">Он должен быть идентификатором, если каталог является корневым каталогом.</span><span class="sxs-lookup"><span data-stu-id="28b69-106">It must be an identifier if the directory is a root directory.</span></span> <span data-ttu-id="28b69-107">Если каталог не является корневым, это значение должно быть парой имя файла или имя файла: имя файла.</span><span class="sxs-lookup"><span data-stu-id="28b69-107">If the directory is a non-root, this value must be a filename or a filename:filename pair.</span></span> <span data-ttu-id="28b69-108">Обратите внимание, что "." допускается в качестве имени файла и имеет специальное значение в таблице Directory.</span><span class="sxs-lookup"><span data-stu-id="28b69-108">Note that "." is allowed as a file name and has special meaning in the Directory table.</span></span>

 

 



