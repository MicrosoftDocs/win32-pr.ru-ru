---
title: Загрузка символа по умолчанию
description: Загрузка символа по умолчанию
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 387715b5078c4ec875c9abce47039898e4998cf7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700549"
---
# <a name="loading-the-default-character"></a><span data-ttu-id="fabe0-103">Загрузка символа по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fabe0-103">Loading the Default Character</span></span>

<span data-ttu-id="fabe0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fabe0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fabe0-105">Вместо того чтобы загружать только конкретный символ непосредственно, указав его имя файла, можно загрузить *символ по умолчанию*.</span><span class="sxs-lookup"><span data-stu-id="fabe0-105">Instead of loading only a specific character directly by specifying its filename, you can load the *default character*.</span></span> <span data-ttu-id="fabe0-106">Символ по умолчанию — это служба, предназначенная для предоставления общего, центрального помощника Windows, который выбирает пользователь.</span><span class="sxs-lookup"><span data-stu-id="fabe0-106">The default character is a service intended to provide a shared, central Windows assistant that the user chooses.</span></span> <span data-ttu-id="fabe0-107">Microsoft Agent включает страницу свойств как часть службы символов по умолчанию, которая называется символом окно свойств, что позволяет пользователю изменить свой выбор символа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fabe0-107">Microsoft Agent includes a property sheet as part of the default character service, known as the Character Properties window, which enables the user to change their selection of the default character.</span></span>

<span data-ttu-id="fabe0-108">Выбор символа по умолчанию ограничен символом, поддерживающим стандартный набор анимации, что обеспечивает базовый уровень согласованности между символами.</span><span class="sxs-lookup"><span data-stu-id="fabe0-108">Selection of the default character is limited to a character that supports the standard animation set, ensuring a basic level of consistency across characters.</span></span> <span data-ttu-id="fabe0-109">Это не исключает использование символа для дополнительных анимаций.</span><span class="sxs-lookup"><span data-stu-id="fabe0-109">This does not exclude a character from having additional animations.</span></span>

<span data-ttu-id="fabe0-110">Однако, поскольку символ по умолчанию предназначен для общего использования и может совместно использоваться другими приложениями одновременно, не загружая символ по умолчанию, если требуется, чтобы символ был исключительно для приложения.</span><span class="sxs-lookup"><span data-stu-id="fabe0-110">However, because the default character is intended for general-purpose use and may be shared by other applications at the same time, avoid loading the default character when you want a character exclusively for your application.</span></span>

<span data-ttu-id="fabe0-111">Чтобы загрузить символ по умолчанию, вызовите метод [**Load**](load-method.md) без указания имени файла или пути.</span><span class="sxs-lookup"><span data-stu-id="fabe0-111">To load the default character, call the [**Load**](load-method.md) method without specifying a filename or path.</span></span> <span data-ttu-id="fabe0-112">Microsoft Agent автоматически загружает текущий набор символов в качестве символа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fabe0-112">Microsoft Agent automatically loads the current character set as the default character.</span></span> <span data-ttu-id="fabe0-113">Если пользователь еще не выбрал символ по умолчанию, то агент выберет первый символ, поддерживающий стандартный набор эффектов анимации.</span><span class="sxs-lookup"><span data-stu-id="fabe0-113">If the user has not yet selected a default character, Agent will select the first character that supports the standard animation set.</span></span> <span data-ttu-id="fabe0-114">Если она недоступна, метод завершится ошибкой и сообщит о причинах.</span><span class="sxs-lookup"><span data-stu-id="fabe0-114">If none is available, the method will fail and report back the cause.</span></span>

<span data-ttu-id="fabe0-115">Хотя клиентское приложение может запросить идентификатор символа, только пользователь может изменить его параметры.</span><span class="sxs-lookup"><span data-stu-id="fabe0-115">Although a client application can inquire as to the identity of the character, only a user can change its settings.</span></span> <span data-ttu-id="fabe0-116">Для вывода окно свойств символов можно использовать [**шовдефаултчарактерпропертиес**](showdefaultcharacterproperties-method.md) .</span><span class="sxs-lookup"><span data-stu-id="fabe0-116">You can use the [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) to display the Character Properties window.</span></span>

<span data-ttu-id="fabe0-117">Сервер будет уведомлять клиентов, которые загрузили символ по умолчанию, когда пользователь изменяет выбор символов, и передает идентификатор GUID нового символа.</span><span class="sxs-lookup"><span data-stu-id="fabe0-117">The server will notify clients that have loaded the default character when a user changes a character selection, and pass the GUID of the new character.</span></span> <span data-ttu-id="fabe0-118">Сервер автоматически выгружает первый символ и перезагружает новый.</span><span class="sxs-lookup"><span data-stu-id="fabe0-118">The server automatically unloads the former character and reloads the new character.</span></span> <span data-ttu-id="fabe0-119">Очереди всех клиентов, которые загрузили символ по умолчанию, прерываются и сбрасываются.</span><span class="sxs-lookup"><span data-stu-id="fabe0-119">The queues of any clients that have loaded the default character are halted and flushed.</span></span> <span data-ttu-id="fabe0-120">Однако не затрагиваются очереди клиентов, которые загрузили символ явным образом с использованием имени файла символа.</span><span class="sxs-lookup"><span data-stu-id="fabe0-120">However, the queues of clients that have loaded the character explicitly using the character's filename are not affected.</span></span> <span data-ttu-id="fabe0-121">При необходимости сервер также автоматически выполняет сброс подсистемы преобразования текста в речь (TTS) для нового символа.</span><span class="sxs-lookup"><span data-stu-id="fabe0-121">If necessary, the server also handles automatically resetting the text-to-speech (TTS) engine for the new character.</span></span>

 

 




