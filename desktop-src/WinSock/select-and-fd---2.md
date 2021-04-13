---
description: Так как сокеты не представлены в формате UNIX, небольшое неотрицательное целое число, реализация функции SELECT была изменена в сокетах Windows.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Макросы SELECT, FD_SET и FD_XXX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544863"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a><span data-ttu-id="d3b62-103">Макросы SELECT, ДЕМОна \_ Set и демона \_ xxx</span><span class="sxs-lookup"><span data-stu-id="d3b62-103">Select, FD\_SET, and FD\_XXX Macros</span></span>

<span data-ttu-id="d3b62-104">Так как сокеты не представлены в формате UNIX, небольшое неотрицательное целое число, реализация функции [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) была изменена в сокетах Windows.</span><span class="sxs-lookup"><span data-stu-id="d3b62-104">Since sockets are not represented by the UNIX-style, small, non-negative integer, the implementation of the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was changed in Windows Sockets.</span></span> <span data-ttu-id="d3b62-105">Каждый набор сокетов по-прежнему представлен структурой **\_ набора** элементов, но вместо сохранения в виде битовой маски набор реализуется как массив сокетов.</span><span class="sxs-lookup"><span data-stu-id="d3b62-105">Each set of sockets is still represented by the **FD\_SET** structure, but instead of being stored as a bitmask, the set is implemented as an array of sockets.</span></span> <span data-ttu-id="d3b62-106">Чтобы избежать потенциальных проблем, приложения должны придерживаться использования макросов ДЕМОна \_ xxx для установки, инициализации, очистки и проверки структур наборов элементов [**фильтра \_**](/windows/desktop/api/winsock/nf-winsock-fd_set) .</span><span class="sxs-lookup"><span data-stu-id="d3b62-106">To avoid potential problems, applications must adhere to the use of the FD\_XXX macros to set, initialize, clear, and check the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3b62-107">См. также</span><span class="sxs-lookup"><span data-stu-id="d3b62-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3b62-108">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="d3b62-108">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="d3b62-109">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="d3b62-109">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



