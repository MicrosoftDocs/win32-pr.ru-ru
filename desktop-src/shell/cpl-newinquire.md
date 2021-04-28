---
description: CPL_NEWINQUIRE сообщение — отправляется функции Кплапплет приложения панели управления для запроса сведений о диалоговом окне, которое поддерживает приложение.
title: Сообщение CPL_NEWINQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104442"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="9ee12-103">\_Сообщение CPL невинкуире</span><span class="sxs-lookup"><span data-stu-id="9ee12-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="9ee12-104">Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления для запроса сведений о диалоговом окне, которое поддерживает приложение.</span><span class="sxs-lookup"><span data-stu-id="9ee12-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ee12-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ee12-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ee12-106">*уаппнум*</span><span class="sxs-lookup"><span data-stu-id="9ee12-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee12-107">Число в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="9ee12-107">The dialog box number.</span></span> <span data-ttu-id="9ee12-108">Это число должно находиться в диапазоне от нуля до значения, возвращенного в ответ на сообщение [**CPL \_ NOCOUNT**](cpl-getcount.md) (CPL \_ -count – 1).</span><span class="sxs-lookup"><span data-stu-id="9ee12-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-109">*лпнкпли*</span><span class="sxs-lookup"><span data-stu-id="9ee12-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee12-110">Адрес структуры [**невкплинфо**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9ee12-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="9ee12-111">Приложение панели управления должно заполнить эту структуру сведениями о диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="9ee12-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ee12-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ee12-112">Return value</span></span>

<span data-ttu-id="9ee12-113">Если функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) успешно обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="9ee12-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ee12-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="9ee12-114">Remarks</span></span>

<span data-ttu-id="9ee12-115">Для повышения производительности большинство приложений должны игнорировать **CPL \_ невинкуире** и обрабатывать сообщение о [**\_ запросах CPL**](cpl-inquire.md) .</span><span class="sxs-lookup"><span data-stu-id="9ee12-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="9ee12-116">Панель управления отправляет сообщение **CPL \_ невинкуире** один раз для каждого диалогового окна, поддерживаемого приложением.</span><span class="sxs-lookup"><span data-stu-id="9ee12-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="9ee12-117">Панель управления также отправляет сообщение о [**\_ запросах CPL**](cpl-inquire.md) для каждого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="9ee12-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="9ee12-118">Эти сообщения отправляются сразу после сообщения [**CPL. \_ Count**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="9ee12-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="9ee12-119">Однако система не гарантирует, что порядок отправки сообщений CPL **\_ Невинкуире и CPL** . **\_**</span><span class="sxs-lookup"><span data-stu-id="9ee12-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="9ee12-120">При получении запроса [**CPL \_**](cpl-inquire.md)можно выполнить инициализацию этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="9ee12-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="9ee12-121">Если необходимо выделить память, сделайте это в ответ на сообщение [**CPL \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="9ee12-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="9ee12-122">[**CPL \_ ЗАПРОС**](cpl-inquire.md) является предпочтительным сообщением.</span><span class="sxs-lookup"><span data-stu-id="9ee12-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="9ee12-123">Это обусловлено тем, что **CPL \_ невинкуире** возвращает сведения в форме, которую система не может кэшировать.</span><span class="sxs-lookup"><span data-stu-id="9ee12-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="9ee12-124">Следовательно, приложения, обрабатывающие **CPL \_ невинкуире** , должны загружаться каждый раз, когда на панели управления потребуются сведения, что приводит к значительному снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="9ee12-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="9ee12-125">Единственными приложениями, которые должны использовать **CPL \_ невинкуире** , являются те, которые требуют изменения значков или отображения строк на основе состояния компьютера.</span><span class="sxs-lookup"><span data-stu-id="9ee12-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="9ee12-126">В этом случае обработчик [**\_ запросов CPL**](cpl-inquire.md) должен указать \_ динамическое \_ значение Res для элементов **Идикон**, **иднаме** или **идинфо** структуры [**кплинфо**](/windows/win32/api/cpl/ns-cpl-cplinfo) вместо того, чтобы указывать допустимый идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ee12-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="9ee12-127">Это приводит к тому, что панель управления отправляет сообщение **CPL \_ невинкуире** каждый раз, когда ему требуется значок и отображаемые строки, что позволяет указать сведения на основе текущего состояния компьютера.</span><span class="sxs-lookup"><span data-stu-id="9ee12-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="9ee12-128">Разумеется, это значительно медленнее, чем использование кэшированных данных.</span><span class="sxs-lookup"><span data-stu-id="9ee12-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ee12-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9ee12-129">Requirements</span></span>



| <span data-ttu-id="9ee12-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9ee12-130">Requirement</span></span> | <span data-ttu-id="9ee12-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9ee12-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9ee12-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ee12-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee12-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ee12-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9ee12-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ee12-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee12-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ee12-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9ee12-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9ee12-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ee12-137"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ee12-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
