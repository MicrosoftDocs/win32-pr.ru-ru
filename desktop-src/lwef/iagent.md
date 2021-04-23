---
title: иажент
description: иажент
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330019"
---
# <a name="iagent"></a><span data-ttu-id="1bbad-103">иажент</span><span class="sxs-lookup"><span data-stu-id="1bbad-103">IAgent</span></span>

<span data-ttu-id="1bbad-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1bbad-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="1bbad-105">**Иажент** определяет интерфейс, позволяющий приложениям загружать символы, принимать события и проверять текущее состояние сервера Microsoft Agent Server.</span><span class="sxs-lookup"><span data-stu-id="1bbad-105">**IAgent** defines an interface that allows applications to load characters, receive events, and check the current state of the Microsoft Agent Server.</span></span> <span data-ttu-id="1bbad-106">Эти функции также доступны из [**иажентекс**](iagentex.md).</span><span class="sxs-lookup"><span data-stu-id="1bbad-106">These functions are also available from [**IAgentEx**](iagentex.md).</span></span>

<span data-ttu-id="1bbad-107">Метод приостановки, включенный в предыдущие версии, устарел и возвращает **значение false** для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="1bbad-107">The GetSuspended method included in previous versions is obsolete and returns **False** for backward compatibility.</span></span>

<span data-ttu-id="1bbad-108">**Методы в порядке таблицы Vtable**</span><span class="sxs-lookup"><span data-stu-id="1bbad-108">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="1bbad-109">Методы Иажент</span><span class="sxs-lookup"><span data-stu-id="1bbad-109">IAgent Methods</span></span>                               | <span data-ttu-id="1bbad-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1bbad-110">Description</span></span>                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="1bbad-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="1bbad-111">**Load**</span></span>](load-method.md)                  | <span data-ttu-id="1bbad-112">Загружает файл данных символа.</span><span class="sxs-lookup"><span data-stu-id="1bbad-112">Loads a character's data file.</span></span>                                |
| [<span data-ttu-id="1bbad-113">**Надстройк**</span><span class="sxs-lookup"><span data-stu-id="1bbad-113">**Unload**</span></span>](unload-method.md)              | <span data-ttu-id="1bbad-114">Выгружает файл данных символа.</span><span class="sxs-lookup"><span data-stu-id="1bbad-114">Unloads a character's data file.</span></span>                              |
| [<span data-ttu-id="1bbad-115">**Регистрация**</span><span class="sxs-lookup"><span data-stu-id="1bbad-115">**Register**</span></span>](iagent--register.md)         | <span data-ttu-id="1bbad-116">Регистрирует приемник уведомлений для клиента.</span><span class="sxs-lookup"><span data-stu-id="1bbad-116">Registers a notification sink for the client.</span></span>                 |
| [<span data-ttu-id="1bbad-117">**унегистер**</span><span class="sxs-lookup"><span data-stu-id="1bbad-117">**Unegister**</span></span>](iagent--unregister.md)      | <span data-ttu-id="1bbad-118">Отменяет регистрацию приемника уведомлений клиента.</span><span class="sxs-lookup"><span data-stu-id="1bbad-118">Unregisters a client's notification sink.</span></span>                     |
| [<span data-ttu-id="1bbad-119">**Символ**</span><span class="sxs-lookup"><span data-stu-id="1bbad-119">**GetCharacter**</span></span>](iagent--getcharacter.md) | <span data-ttu-id="1bbad-120">Возвращает интерфейс Иажентчарактер для загруженного символа.</span><span class="sxs-lookup"><span data-stu-id="1bbad-120">Returns the IAgentCharacter interface for a loaded character.</span></span> |



 

 

 




