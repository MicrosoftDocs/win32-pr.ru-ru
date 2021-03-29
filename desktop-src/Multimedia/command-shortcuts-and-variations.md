---
title: Ярлыки и варианты команд
description: Ярлыки и варианты команд
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778065"
---
# <a name="command-shortcuts-and-variations"></a><span data-ttu-id="09e81-103">Ярлыки и варианты команд</span><span class="sxs-lookup"><span data-stu-id="09e81-103">Command Shortcuts and Variations</span></span>

<span data-ttu-id="09e81-104">При работе с командами MCI можно использовать несколько сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="09e81-104">You can use several shortcuts when working with MCI commands.</span></span> <span data-ttu-id="09e81-105">Эти сочетания клавиш позволяют использовать один идентификатор для ссылки на все устройства, открытые приложением, или для открытия устройства без явного [**запуска команды Open**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="09e81-105">These shortcuts enable you to use a single identifier to refer to all the devices your application has opened, or to open a device without explicitly issuing an [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="09e81-106">\_ \_ \_ Для любой команды, не возвращающей сведения, можно указать значение "ALL" (идентификатор устройства MCI) в качестве идентификатора устройства.</span><span class="sxs-lookup"><span data-stu-id="09e81-106">You can specify "all" (MCI\_ALL\_DEVICE\_ID) as a device identifier for any command that does not return information.</span></span> <span data-ttu-id="09e81-107">При указании «ALL» MCI отправляет команду последовательно на все устройства, открытые текущим приложением.</span><span class="sxs-lookup"><span data-stu-id="09e81-107">When you specify "all", MCI sends the command sequentially to all devices opened by the current application.</span></span>

<span data-ttu-id="09e81-108">Например, команда [**Close**](close.md) "все" закрывает все открытые устройства, а команда " [**воспроизвести**](play.md) все" запускает воспроизведение всех устройств, открытых приложением.</span><span class="sxs-lookup"><span data-stu-id="09e81-108">For example, the [**close**](close.md) "all" command closes all open devices and the [**play**](play.md) "all" command starts playing all devices opened by the application.</span></span> <span data-ttu-id="09e81-109">Так как MCI последовательно отправляет команды на устройства MCI, между первым и последним устройствами, получающими команду, существует интервал.</span><span class="sxs-lookup"><span data-stu-id="09e81-109">Because MCI sequentially sends the commands to the MCI devices, there is an interval between when the first and last devices receive the command.</span></span>

<span data-ttu-id="09e81-110">Использование «ALL» — удобный способ вещания команды на все устройства, но не следует полагаться на нее для синхронизации устройств; время между сообщениями может отличаться.</span><span class="sxs-lookup"><span data-stu-id="09e81-110">Using "all" is a convenient way to broadcast a command to all your devices, but you should not rely on it to synchronize devices; the timing between messages can vary.</span></span>

<span data-ttu-id="09e81-111">Когда вы выдаете команду и указываете неоткрытое устройство, MCI пытается открыть устройство перед реализацией команды.</span><span class="sxs-lookup"><span data-stu-id="09e81-111">When you issue a command and specify a device that is not open, MCI tries to open the device before implementing the command.</span></span> <span data-ttu-id="09e81-112">Для автоматического открытия устройств применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="09e81-112">The following rules apply to automatically opening devices:</span></span>

-   <span data-ttu-id="09e81-113">Функция автоматического открытия работает только с интерфейсом командной строки.</span><span class="sxs-lookup"><span data-stu-id="09e81-113">The automatic open feature works only with the command-string interface.</span></span>
-   <span data-ttu-id="09e81-114">Функция автоматического открытия не работает для команд, характерных для пользовательских драйверов устройств.</span><span class="sxs-lookup"><span data-stu-id="09e81-114">The automatic open feature fails for commands that are specific to custom device drivers.</span></span>
-   <span data-ttu-id="09e81-115">Автоматически открытые устройства не отвечают на команды, в которых в качестве имени устройства используется "все".</span><span class="sxs-lookup"><span data-stu-id="09e81-115">Automatically opened devices do not respond to commands that use "all" as a device name.</span></span>
-   <span data-ttu-id="09e81-116">Функция автоматического открытия не позволяет приложению задавать флаг "Type".</span><span class="sxs-lookup"><span data-stu-id="09e81-116">The automatic open feature does not let your application specify the "type" flag.</span></span> <span data-ttu-id="09e81-117">Без имени устройства MCI определяет имя устройства из записей в реестре.</span><span class="sxs-lookup"><span data-stu-id="09e81-117">Without the device name, MCI determines the device name from the entries in the registry.</span></span> <span data-ttu-id="09e81-118">Чтобы использовать конкретное устройство, можно объединить имя устройства с именем файла, используя восклицательный знак, как описано в справочном материале по команде [**Open**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="09e81-118">To use a specific device, you can combine the device name with the filename by using the exclamation point, as described in the reference material for the [**open**](open.md) command.</span></span>

<span data-ttu-id="09e81-119">Если приложение использует функцию автоматического открытия для открытия устройства, приложение должно проверить возвращаемое значение каждой последующей команды Open, чтобы убедиться, что устройство по-прежнему открыто.</span><span class="sxs-lookup"><span data-stu-id="09e81-119">If an application uses the automatic open feature to open a device, the application should check the return value of every subsequent open command to verify that the device is still open.</span></span> <span data-ttu-id="09e81-120">Кроме того, MCI автоматически закрывает все автоматически открываемые устройства.</span><span class="sxs-lookup"><span data-stu-id="09e81-120">MCI also automatically closes any device that it automatically opens.</span></span> <span data-ttu-id="09e81-121">MCI обычно закрывает устройство в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="09e81-121">MCI typically closes a device in the following situations:</span></span>

-   <span data-ttu-id="09e81-122">Команда завершена.</span><span class="sxs-lookup"><span data-stu-id="09e81-122">The command is completed.</span></span>
-   <span data-ttu-id="09e81-123">Команда прерывается.</span><span class="sxs-lookup"><span data-stu-id="09e81-123">You abort the command.</span></span>
-   <span data-ttu-id="09e81-124">Вы запрашиваете уведомление в последующей команде.</span><span class="sxs-lookup"><span data-stu-id="09e81-124">You request notification in a subsequent command.</span></span>
-   <span data-ttu-id="09e81-125">MCI обнаруживает сбой.</span><span class="sxs-lookup"><span data-stu-id="09e81-125">MCI detects a failure.</span></span>

 

 




