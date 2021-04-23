---
description: Можно написать собственную программу создания хранилища символов, а не использовать SymStore.
ms.assetid: 5ccd0e41-3ae7-44b1-a72e-f59963340731
title: Использование других хранилищ символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63724e97ddcc6d2cf660c6a808c5320d7638e8ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990559"
---
# <a name="using-other-symbol-stores"></a><span data-ttu-id="ae8ee-103">Использование других хранилищ символов</span><span class="sxs-lookup"><span data-stu-id="ae8ee-103">Using Other Symbol Stores</span></span>

<span data-ttu-id="ae8ee-104">Можно написать собственную программу создания хранилища символов, а не использовать SymStore.</span><span class="sxs-lookup"><span data-stu-id="ae8ee-104">It is possible to write your own symbol store creation program, rather than using SymStore.</span></span>

<span data-ttu-id="ae8ee-105">Так как транзакции SymStore все зарегистрированы в текстовых файлах в формате CSV, можно использовать любые существующие файлы журнала SymStore для использования в собственной программе для работы с базами данных.</span><span class="sxs-lookup"><span data-stu-id="ae8ee-105">Since SymStore transactions are all logged in CSV-format text files, you can leverage any existing SymStore log files for use in your own database program.</span></span>

<span data-ttu-id="ae8ee-106">Если вы планируете использовать программу SymSrv, предоставляемую с инструментами отладки для Windows, рекомендуется также использовать SymStore.</span><span class="sxs-lookup"><span data-stu-id="ae8ee-106">If you plan to use the SymSrv program provided with Debugging Tools for Windows, it is recommended that you use SymStore as well.</span></span> <span data-ttu-id="ae8ee-107">Обновления этих двух программ всегда будут выпущены вместе, поэтому их версии будут всегда совпадать.</span><span class="sxs-lookup"><span data-stu-id="ae8ee-107">Updates to these two programs will always be released together, and therefore their versions will always match.</span></span>

 

 



