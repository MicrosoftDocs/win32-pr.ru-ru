---
title: Обработка подключения к оконной станции
description: Процесс автоматически устанавливает соединение с рабочей станцией и настольным компьютером при первом вызове функции USER32 или GDI32 (за исключением оконных функций и рабочих станций).
ms.assetid: 280f69e7-5c99-41a7-94e3-da13deaac9f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a87e97b19ac1210b04447652268c5f53b7e2a6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413382"
---
# <a name="process-connection-to-a-window-station"></a><span data-ttu-id="51728-103">Обработка подключения к оконной станции</span><span class="sxs-lookup"><span data-stu-id="51728-103">Process Connection to a Window Station</span></span>

<span data-ttu-id="51728-104">Процесс автоматически устанавливает соединение с рабочей станцией и настольным компьютером при первом вызове функции USER32 или GDI32 (за исключением оконных функций и рабочих станций).</span><span class="sxs-lookup"><span data-stu-id="51728-104">A process automatically establishes a connection to a window station and desktop when it first calls a USER32 or GDI32 function (other than the window station and desktop functions).</span></span> <span data-ttu-id="51728-105">Система определяет станцию Windows, к которой процесс подключается в соответствии со следующими правилами.</span><span class="sxs-lookup"><span data-stu-id="51728-105">The system determines the window station to which a process connects according to the following rules:</span></span>

1.  <span data-ttu-id="51728-106">Если процесс вызвал функцию [**сетпроцессвиндовстатион**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) , он подключается к станции окна, указанной в этом вызове.</span><span class="sxs-lookup"><span data-stu-id="51728-106">If the process has called the [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) function, it connects to the window station specified in that call.</span></span>
2.  <span data-ttu-id="51728-107">Если процесс не вызывал [**сетпроцессвиндовстатион**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation), он подключается к станции окна, унаследованной от родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="51728-107">If the process did not call [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation), it connects to the window station inherited from the parent process.</span></span>
3.  <span data-ttu-id="51728-108">Если процесс не вызывал [**сетпроцессвиндовстатион**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) и не наследовал станцию окна, система пытается открыть для максимального \_ разрешенного доступа и подключиться к станции Windows следующим образом:</span><span class="sxs-lookup"><span data-stu-id="51728-108">If the process did not call [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) and did not inherit a window station, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a window station as follows:</span></span>
    -   <span data-ttu-id="51728-109">Если имя станции Windows было указано в элементе **лпдесктоп** структуры [**стартупинфо**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) , которая использовалась при создании процесса, процесс подключается к указанной рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="51728-109">If a window station name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the process connects to the specified window station.</span></span>
    -   <span data-ttu-id="51728-110">В противном случае, если процесс выполняется в сеансе входа интерактивного пользователя, этот процесс подключается к интерактивной рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="51728-110">Otherwise, if the process is running in the logon session of the interactive user, the process connects to the interactive window station.</span></span>
    -   <span data-ttu-id="51728-111">Если процесс выполняется в неинтерактивном сеансе входа, имя Windows Station Name формируется на основе идентификатора сеанса входа в систему и предпринимается попытка открыть эту станцию окон.</span><span class="sxs-lookup"><span data-stu-id="51728-111">If the process is running in a noninteractive logon session, the window station name is formed based on the logon session identifier and an attempt is made to open that window station.</span></span> <span data-ttu-id="51728-112">Если операция открытия завершается сбоем, так как эта станция окна не существует, система пытается создать оконную станцию и Рабочий стол по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51728-112">If the open operation fails because this window station does not exist, the system tries to create the window station and a default desktop.</span></span>

<span data-ttu-id="51728-113">Станция окна, назначенная во время этого процесса подключения, не может быть закрыта путем вызова функции [**клосевиндовстатион**](/windows/win32/api/winuser/nf-winuser-closewindowstation) .</span><span class="sxs-lookup"><span data-stu-id="51728-113">The window station assigned during this connection process cannot be closed by calling the [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) function.</span></span>

<span data-ttu-id="51728-114">При подключении процесса к Windows-станции система выполняет поиск наследуемых дескрипторов в таблице дескрипторов процесса.</span><span class="sxs-lookup"><span data-stu-id="51728-114">When a process is connecting to a window station, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="51728-115">Система использует первый найденный обработчик оконной станции.</span><span class="sxs-lookup"><span data-stu-id="51728-115">The system uses the first window station handle it finds.</span></span> <span data-ttu-id="51728-116">Если требуется, чтобы дочерний процесс подключаться к определенной наследуемой станции окна, необходимо убедиться, что только нужный маркер помечен как наследуемый.</span><span class="sxs-lookup"><span data-stu-id="51728-116">If you want a child process to connect to a particular inherited window station, you must ensure that only the desired handle is marked inheritable.</span></span> <span data-ttu-id="51728-117">Если дочерний процесс наследует несколько дескрипторов оконных станций, то результаты подключения Windows Station не определяются.</span><span class="sxs-lookup"><span data-stu-id="51728-117">If a child process inherits multiple window station handles, the results of the window station connection are undefined.</span></span>

<span data-ttu-id="51728-118">Дескрипторы оконной станции, открываемой системой при подключении процесса к рабочей станции, не наследуются.</span><span class="sxs-lookup"><span data-stu-id="51728-118">Handles to a window station that the system opens while connecting a process to a window station are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51728-119">См. также</span><span class="sxs-lookup"><span data-stu-id="51728-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51728-120">Подключение потока к рабочему столу</span><span class="sxs-lookup"><span data-stu-id="51728-120">Thread Connection to a Desktop</span></span>](thread-connection-to-a-desktop.md)
</dt> </dl>

 

 