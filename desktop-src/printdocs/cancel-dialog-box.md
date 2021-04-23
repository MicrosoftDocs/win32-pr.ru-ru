---
description: В этом разделе описывается, как отобразить ход выполнения задания печати пользователю и дать ему возможность отменить задание печати, которое в данный момент выполняется.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: Как отобразить ход выполнения задания печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673693"
---
# <a name="how-to-display-the-print-job-progress"></a><span data-ttu-id="819df-103">Как отобразить ход выполнения задания печати</span><span class="sxs-lookup"><span data-stu-id="819df-103">How To: Display the Print Job Progress</span></span>

<span data-ttu-id="819df-104">В этом разделе описывается, как отобразить ход выполнения задания печати пользователю и дать ему возможность отменить задание печати, которое в данный момент выполняется.</span><span class="sxs-lookup"><span data-stu-id="819df-104">This topic describes how to display the print job progress to the user and give them the option to cancel a print job that is currently in progress.</span></span>

## <a name="overview"></a><span data-ttu-id="819df-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="819df-105">Overview</span></span>

<span data-ttu-id="819df-106">Процедура диалогового окна «ход печати» обычно выполняет следующие функции.</span><span class="sxs-lookup"><span data-stu-id="819df-106">A print progress dialog procedure typically performs the following functions.</span></span>

-   <span data-ttu-id="819df-107">Отображение хода выполнения задания печати для пользователя.</span><span class="sxs-lookup"><span data-stu-id="819df-107">Display print job progress to the user.</span></span>
-   <span data-ttu-id="819df-108">Запустите поток обработки печати.</span><span class="sxs-lookup"><span data-stu-id="819df-108">Start the print processing thread.</span></span>
-   <span data-ttu-id="819df-109">Отобразить кнопку **Отмена** , чтобы пользователь мог остановить задание печати до его завершения.</span><span class="sxs-lookup"><span data-stu-id="819df-109">Display a **Cancel** button so the user can stop a print job before it finishes.</span></span>

<span data-ttu-id="819df-110">Строго говоря, единственным действием, выполняемым в диалоговом окне «ход печати», является отображение хода выполнения задания печати пользователю.</span><span class="sxs-lookup"><span data-stu-id="819df-110">Strictly speaking, the only thing that the print progress dialog box procedure must do is display the print job progress to the user.</span></span> <span data-ttu-id="819df-111">Однако, поскольку две другие функции в приведенном выше списке тесно связаны друг с другом, они также включены в этот модуль.</span><span class="sxs-lookup"><span data-stu-id="819df-111">However, because the other two functions in the preceding list are closely related, they have also been included in this module.</span></span>

## <a name="displaying-print-job-progress"></a><span data-ttu-id="819df-112">Отображение хода выполнения задания печати</span><span class="sxs-lookup"><span data-stu-id="819df-112">Displaying Print Job Progress</span></span>

<span data-ttu-id="819df-113">Процедура диалогового окна «ход печати» обрабатывает следующие сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="819df-113">A print progress dialog box procedure handles the following window messages.</span></span>

-   <span data-ttu-id="819df-114">**WM \_ инитдиалог**</span><span class="sxs-lookup"><span data-stu-id="819df-114">**WM\_INITDIALOG**</span></span>

    <span data-ttu-id="819df-115">Инициализирует элементы управления, используемые диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="819df-115">Initializes the controls that the dialog box uses.</span></span>

-   <span data-ttu-id="819df-116">**WM \_ сеткурсор**</span><span class="sxs-lookup"><span data-stu-id="819df-116">**WM\_SETCURSOR**</span></span>

    <span data-ttu-id="819df-117">Устанавливает курсор в указатель, когда пользователь может отменить задание печати и курсор ожидания, когда задание печати находится в точке, где его нельзя отменить.</span><span class="sxs-lookup"><span data-stu-id="819df-117">Sets the cursor to a pointer when the user is able to cancel a print job, and to the wait cursor when the print job is at a point where it cannot be cancelled.</span></span>

-   <span data-ttu-id="819df-118">**Печать \_ \_ начала \_ печати**</span><span class="sxs-lookup"><span data-stu-id="819df-118">**USER\_PRINT\_START\_PRINTING**</span></span>

    <span data-ttu-id="819df-119">Задает параметры индикатора выполнения для задания печати и создает поток печати для начала обработки задания печати.</span><span class="sxs-lookup"><span data-stu-id="819df-119">Sets the progress bar parameters for the print job, and creates the printing thread to start processing the print job.</span></span>

    <span data-ttu-id="819df-120">Это сообщение окна для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="819df-120">This is an application-specific window message.</span></span>

-   <span data-ttu-id="819df-121">**\_команда WM-идканцел**</span><span class="sxs-lookup"><span data-stu-id="819df-121">**WM\_COMMAND - IDCANCEL**</span></span>

    <span data-ttu-id="819df-122">Устанавливает событие Cancel, чтобы сообщить потоку обработки печати отменить задание печати.</span><span class="sxs-lookup"><span data-stu-id="819df-122">Sets the cancel event to tell the print processing thread to cancel the print job.</span></span>

-   <span data-ttu-id="819df-123">**\_ \_ Обновление состояния печати \_ пользователя**</span><span class="sxs-lookup"><span data-stu-id="819df-123">**USER\_PRINT\_STATUS\_UPDATE**</span></span>

    <span data-ttu-id="819df-124">Обновляет индикатор выполнения и текст состояния, чтобы отобразить текущее состояние задания печати.</span><span class="sxs-lookup"><span data-stu-id="819df-124">Updates the progress bar and status text to show the current state of the print job.</span></span>

    <span data-ttu-id="819df-125">Это сообщение окна для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="819df-125">This is an application-specific window message.</span></span>

-   <span data-ttu-id="819df-126">**\_закрытие пользователем печати \_**</span><span class="sxs-lookup"><span data-stu-id="819df-126">**USER\_PRINT\_CLOSING**</span></span>

    <span data-ttu-id="819df-127">Задает текст состояния закрытия в диалоговом окне Ход выполнения, чтобы указать, что задание печати закрывается.</span><span class="sxs-lookup"><span data-stu-id="819df-127">Sets the closing status text in the progress dialog box to indicate that the print job is closing.</span></span>

    <span data-ttu-id="819df-128">Это сообщение окна для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="819df-128">This is an application-specific window message.</span></span>

-   <span data-ttu-id="819df-129">**\_Печать пользователем \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="819df-129">**USER\_PRINT\_COMPLETE**</span></span>

    <span data-ttu-id="819df-130">Отображает сообщение о завершении задания печати для пользователя и освобождает дескрипторы и события, которые использовались в этом задании печати.</span><span class="sxs-lookup"><span data-stu-id="819df-130">Displays the "Print job complete" message to the user, and releases handles and events that were used in this print job.</span></span>

    <span data-ttu-id="819df-131">Это сообщение окна для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="819df-131">This is an application-specific window message.</span></span>

 

 



