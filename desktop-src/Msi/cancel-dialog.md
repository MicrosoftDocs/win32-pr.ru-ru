---
description: Диалоговое окно Отмена подтверждает, что пользователь хочет завершить установку. Это модальное диалоговое окно.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Диалоговое окно отмены
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650710"
---
# <a name="cancel-dialog"></a><span data-ttu-id="9fa74-104">Диалоговое окно отмены</span><span class="sxs-lookup"><span data-stu-id="9fa74-104">Cancel Dialog</span></span>

<span data-ttu-id="9fa74-105">Диалоговое окно **Отмена** подтверждает, что пользователь хочет завершить установку.</span><span class="sxs-lookup"><span data-stu-id="9fa74-105">A **Cancel** dialog box confirms that the user wants to terminate the installation.</span></span> <span data-ttu-id="9fa74-106">Это модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="9fa74-106">This is a modal dialog box.</span></span>

<span data-ttu-id="9fa74-107">Этот тип диалогового окна обычно содержит [элемент управления "текст](text-control.md) " и две [кнопки](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="9fa74-107">This type of dialog box commonly contains a [Text control](text-control.md) and two [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="9fa74-108">Эти две кнопки дают пользователю возможность либо вернуться к последнему диалоговому окну, либо подтвердить завершение установки.</span><span class="sxs-lookup"><span data-stu-id="9fa74-108">The two buttons give the user the choice of either returning to the last dialog box or confirming the termination of the installation.</span></span>

<span data-ttu-id="9fa74-109">[EndDialog](enddialog-controlevent.md) таблице ControlEvent событие связан с этими двумя кнопками в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="9fa74-109">The [EndDialog](enddialog-controlevent.md) ControlEvent is linked to these two buttons in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="9fa74-110">*Возвращаемый* параметр EndDialog таблице ControlEvent событие связан с одной из кнопок и вызывает завершение диалогового окна **Отмена** и фокус возврата к предыдущему диалоговому окну.</span><span class="sxs-lookup"><span data-stu-id="9fa74-110">The *Return* parameter of the EndDialog ControlEvent is linked to one of the buttons and causes the **Cancel** dialog box to be terminated and the focus to return to the previous dialog box.</span></span> <span data-ttu-id="9fa74-111">Параметр *Exit* связан с другой кнопкой и заставляет пользовательский интерфейс вернуть управление в установщик с соответствующим кодом, указывающим, что пользователь хочет выйти из программы.</span><span class="sxs-lookup"><span data-stu-id="9fa74-111">The *Exit* parameter is linked to the other button and causes the user interface to return control to the installer with the appropriate code indicating that the user wants to exit.</span></span> <span data-ttu-id="9fa74-112">Затем программа установки завершает работу и отображает [диалоговое окно усерексит](userexit-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="9fa74-112">The installer then shuts down and displays the [UserExit Dialog](userexit-dialog.md).</span></span>

 

 



