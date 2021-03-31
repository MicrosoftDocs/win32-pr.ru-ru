---
description: Подпрограммы обратного вызова очереди по умолчанию обрабатывают уведомления, отправляемые Сетупкоммитфилекуеуе обычным способом.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: О подпрограммых обратного вызова очереди по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897146"
---
# <a name="about-the-default-queue-callback-routine"></a><span data-ttu-id="c387d-103">О подпрограммых обратного вызова очереди по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c387d-103">About the Default Queue Callback Routine</span></span>

<span data-ttu-id="c387d-104">Подпрограммы обратного вызова очереди по умолчанию обрабатывают уведомления, отправляемые [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) обычным способом.</span><span class="sxs-lookup"><span data-stu-id="c387d-104">The default queue callback routine handles notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in a generic manner.</span></span> <span data-ttu-id="c387d-105">Используя подпрограммы по умолчанию, вы получаете готовый пользовательский интерфейс для создания стандартных диалоговых окон установки.</span><span class="sxs-lookup"><span data-stu-id="c387d-105">By using the default routine, you get a ready-made user interface to create common setup dialog boxes.</span></span> <span data-ttu-id="c387d-106">Рекомендуется использовать подпрограммы обратного вызова очереди по умолчанию, как для простоты использования, так и для обеспечения согласованного внешнего вида и поведения диалоговых окон, созданных во время установки.</span><span class="sxs-lookup"><span data-stu-id="c387d-106">It is recommended that you use the default queue callback routine, both for ease of use, and to ensure a consistent appearance and behavior of dialog boxes generated during the installation.</span></span>

<span data-ttu-id="c387d-107">Подпрограмме обратного вызова по умолчанию требуется структура контекста для внутреннего хранения записей.</span><span class="sxs-lookup"><span data-stu-id="c387d-107">The default callback routine requires a context structure for internal record keeping.</span></span> <span data-ttu-id="c387d-108">Кроме того, очередь передает дополнительные сведения, относящиеся к текущему уведомлению, в наборе параметров, *param1* и *Param2*.</span><span class="sxs-lookup"><span data-stu-id="c387d-108">In addition, the queue passes additional information relevant to the current notification in a set of parameters, *Param1* and *Param2*.</span></span>

<span data-ttu-id="c387d-109">Например, если очередь отправляет \_ уведомление спфиленотифи нидмедиа в подпрограммы обратного вызова по умолчанию, параметр *param1* указывает на [**исходную структуру \_ носителя**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) , содержащую сведения о необходимых носителях, а *Param2* указывает на массив символов, который может получить от пользователя новые сведения о пути.</span><span class="sxs-lookup"><span data-stu-id="c387d-109">For example, if the queue sends an SPFILENOTIFY\_NEEDMEDIA notification to the default callback routine, *Param1* points to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure that contains information about the media needed, and *Param2* points to a character array that can receive new path information from the user.</span></span>

<span data-ttu-id="c387d-110">Подсистема обратного вызова по умолчанию использует эти сведения, чтобы предложить пользователю вставить необходимый исходный носитель, указать новый путь, пропустить копирование текущего файла или отменить текущую операцию.</span><span class="sxs-lookup"><span data-stu-id="c387d-110">The default callback routine uses this information to prompt the user to either insert the needed source media, specify a new path, skip copying the current file, or cancel the current operation.</span></span> <span data-ttu-id="c387d-111">Процедура обратного вызова очереди по умолчанию возвращает ФИЛЕОП \_ NewPath, филеоп \_ ДОИТ, филеоп \_ Skip или филеоп \_ Abort в очередь в зависимости от того, какое действие выполнял пользователь.</span><span class="sxs-lookup"><span data-stu-id="c387d-111">The default queue callback routine returns FILEOP\_NEWPATH, FILEOP\_DOIT , FILEOP\_SKIP, or FILEOP\_ABORT to the queue, depending on which action the user took.</span></span>

<span data-ttu-id="c387d-112">Сведения о том, как подпрограммы обратного вызова очереди по умолчанию обрабатывают уведомления каждого из очередей, см. в разделе [уведомления очереди файлов](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c387d-112">For information on how the default queue callback routine handles each queue notification, see [File Queue Notifications](file-queue-notifications.md).</span></span>

<span data-ttu-id="c387d-113">Дополнительные сведения о подфункциях обратного вызова настраиваемой очереди см. [в разделе Создание подпрограммы обратного вызова пользовательской очереди](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="c387d-113">For information on custom queue callback routines, see [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



