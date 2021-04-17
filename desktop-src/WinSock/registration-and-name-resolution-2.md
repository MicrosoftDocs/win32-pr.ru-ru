---
description: Сокеты Windows 2 — это набор функций, которые стандартизируют способ доступа приложений к различным службам именования сетевых имен и их использования.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Регистрация и разрешение имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702015"
---
# <a name="registration-and-name-resolution"></a><span data-ttu-id="21b2c-103">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="21b2c-103">Registration and Name Resolution</span></span>

<span data-ttu-id="21b2c-104">Сокеты Windows 2 — это набор функций, которые стандартизируют способ доступа приложений к различным службам именования сетевых имен и их использования.</span><span class="sxs-lookup"><span data-stu-id="21b2c-104">Windows Sockets 2 is a set of functions that standardizes the way applications access and use the various network naming services.</span></span> <span data-ttu-id="21b2c-105">При использовании этих функций приложения не должны отличать широко отличающиеся протоколы, связанные с такими службами имен, как DNS, NIS, X. 500, SAP и т. д. Чтобы обеспечить полную обратную совместимость с сокетами Windows 1,1, существующие функции **жетксбии** и асинхронной **всаасинкжетксбии** базы данных по-прежнему поддерживаются, но реализуются в интерфейсе поставщика службы Windows Sockets с точки зрения новых возможностей разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="21b2c-105">When using these functions, applications need not distinguish the widely differing protocols associated with name services such as DNS, NIS, X.500, SAP, etc. To maintain full backward compatibility with Windows Sockets 1.1, the existing **getXbyY** and asynchronous **WSAAsyncGetXbyY** database-lookup functions continue to be supported, but are implemented in the Windows Sockets service provider interface in terms of the new name resolution capabilities.</span></span> <span data-ttu-id="21b2c-106">Дополнительные сведения см. в разделе функции [**жетсервбинаме**](/windows/desktop/api/winsock/nf-winsock-getservbyname) и [**жетсервбипорт**](/windows/desktop/api/winsock/nf-winsock-getservbyport) .</span><span class="sxs-lookup"><span data-stu-id="21b2c-106">For more information, see the [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions.</span></span> <span data-ttu-id="21b2c-107">См. также раздел [Совместимость разрешения имен для TCP/IP в сокетах Windows sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span><span class="sxs-lookup"><span data-stu-id="21b2c-107">Also, see [Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span></span>

<span data-ttu-id="21b2c-108">В этом разделе описаны возможности регистрации и разрешения имен, доступные для разработчиков Winsock.</span><span class="sxs-lookup"><span data-stu-id="21b2c-108">This section describes registration and name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="21b2c-109">В следующем списке перечислены подразделы этого раздела.</span><span class="sxs-lookup"><span data-stu-id="21b2c-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="21b2c-110">Разрешение имен, не зависящее от протокола</span><span class="sxs-lookup"><span data-stu-id="21b2c-110">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
-   [<span data-ttu-id="21b2c-111">Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="21b2c-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="21b2c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="21b2c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21b2c-113">Об Winsock</span><span class="sxs-lookup"><span data-stu-id="21b2c-113">About Winsock</span></span>](about-winsock.md)
</dt> <dt>

[<span data-ttu-id="21b2c-114">Использование Winsock</span><span class="sxs-lookup"><span data-stu-id="21b2c-114">Using Winsock</span></span>](using-winsock.md)
</dt> </dl>

 

 



