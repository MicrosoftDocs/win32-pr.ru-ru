---
description: Разработчикам баз данных установки необходимо знать о двух ограничениях на обработку потоков с помощью реализации структурированного хранилища Win32 OLE.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Ограничения для потоков OLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263431"
---
# <a name="ole-limitations-on-streams"></a><span data-ttu-id="3b524-103">Ограничения для потоков OLE</span><span class="sxs-lookup"><span data-stu-id="3b524-103">OLE Limitations on Streams</span></span>

<span data-ttu-id="3b524-104">Разработчикам баз данных установки необходимо знать о двух ограничениях на обработку потоков с помощью реализации структурированного хранилища Win32 OLE.</span><span class="sxs-lookup"><span data-stu-id="3b524-104">Developers of installation databases need to be aware of two limitations on the handling of streams by the Win32 OLE structured storage implementation.</span></span> <span data-ttu-id="3b524-105">Эти ограничения могут повлиять на функции установщика косвенно через преобразования и другие данные, которые могут храниться в базе данных в виде потока.</span><span class="sxs-lookup"><span data-stu-id="3b524-105">These limitations can affect installer functions indirectly through transforms and other data that may be stored in the database as a stream.</span></span>

<span data-ttu-id="3b524-106">Существует два соответствующих ограничения.</span><span class="sxs-lookup"><span data-stu-id="3b524-106">There are two relevant limitations:</span></span>

-   <span data-ttu-id="3b524-107">Двоичные данные хранятся с именем индекса, созданным путем сцепления имени таблицы и значений первичных ключей записи с помощью разделителя точек.</span><span class="sxs-lookup"><span data-stu-id="3b524-107">Binary data is stored with an index name created by concatenating the table name and the values of the record's primary keys using a period delimiter.</span></span> <span data-ttu-id="3b524-108">OLE ограничивает имена потоков до 32 символов (31 + знак завершения null).</span><span class="sxs-lookup"><span data-stu-id="3b524-108">OLE limits stream names to 32 characters (31 + null terminator).</span></span> <span data-ttu-id="3b524-109">Установщик Windows использует алгоритм сжатия, который позволяет увеличить ограничение до 62 символов в зависимости от символа.</span><span class="sxs-lookup"><span data-stu-id="3b524-109">Windows Installer uses a compression algorithm that can expand the limit to 62 characters depending upon the character.</span></span> <span data-ttu-id="3b524-110">Обратите внимание, что двухбайтовые символы считаются 2.</span><span class="sxs-lookup"><span data-stu-id="3b524-110">Note that double-byte characters count as 2.</span></span>
-   <span data-ttu-id="3b524-111">Хотя одновременно можно открыть несколько потоков, вы не сможете открыть поток еще раз, пока первая ссылка не будет закрыта.</span><span class="sxs-lookup"><span data-stu-id="3b524-111">Although you can have multiple streams open at one time, you cannot open a stream a second time until the first reference is closed.</span></span> <span data-ttu-id="3b524-112">Это означает, что нельзя выбрать один поток двоичных данных для одновременного открытия в нескольких записях.</span><span class="sxs-lookup"><span data-stu-id="3b524-112">This means you cannot select the same binary data stream to be open in multiple records simultaneously.</span></span> <span data-ttu-id="3b524-113">Попытка чтения двоичных данных из второй записи завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3b524-113">Attempts to read the binary data from the second record fail.</span></span> <span data-ttu-id="3b524-114">Кроме того, невозможно переименовать первичные ключи записи, пока открыт поток двоичных данных в этой записи.</span><span class="sxs-lookup"><span data-stu-id="3b524-114">Also you cannot rename the primary keys of a record while a binary data stream in that record is open.</span></span>

 

 



