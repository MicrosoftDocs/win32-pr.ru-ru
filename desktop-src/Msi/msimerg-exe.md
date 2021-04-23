---
description: Msimerg.exe — это программа командной строки, которая использует Мсидатабасемерже для слияния эталонной базы данных с базовой базой данных.
ms.assetid: db0c9ae5-a8e8-4eff-ae14-67dcce352483
title: Msimerg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0555aa7bd762b92ed67d0bac1487159fadb73a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999319"
---
# <a name="msimergexe"></a><span data-ttu-id="55e7e-103">Msimerg.exe</span><span class="sxs-lookup"><span data-stu-id="55e7e-103">Msimerg.exe</span></span>

<span data-ttu-id="55e7e-104">Msimerg.exe — это программа командной строки, которая использует [**мсидатабасемерже**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) для [слияния](merges-and-transforms.md) эталонной базы данных с базовой базой данных.</span><span class="sxs-lookup"><span data-stu-id="55e7e-104">Msimerg.exe is a command line utility that uses [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to [merge](merges-and-transforms.md) a reference database into a base database.</span></span>

<span data-ttu-id="55e7e-105">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="55e7e-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55e7e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55e7e-106">Syntax</span></span>

<span data-ttu-id="55e7e-107">**Мсимерг** *{базовая база данных} {эталонная база данных}*</span><span class="sxs-lookup"><span data-stu-id="55e7e-107">**Msimerg** *{base database}{reference database}*</span></span>

<span data-ttu-id="55e7e-108">Если между двумя базами данных существует конфликт слияния, то сведения о конфликте помещаются в \_ таблицу мержееррорс.</span><span class="sxs-lookup"><span data-stu-id="55e7e-108">If there is a merge conflict between the two databases, the conflict information is placed in the \_MergeErrors table.</span></span>

## <a name="command-line-options"></a><span data-ttu-id="55e7e-109">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="55e7e-109">Command Line Options</span></span>

<span data-ttu-id="55e7e-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="55e7e-110">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55e7e-111">См. также</span><span class="sxs-lookup"><span data-stu-id="55e7e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55e7e-112">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="55e7e-112">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="55e7e-113">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="55e7e-113">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



