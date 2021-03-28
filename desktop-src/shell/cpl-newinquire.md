---
description: Отправляется в функцию Кплапплет приложения панели управления для запроса сведений о диалоговом окне, которое поддерживает приложение.
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
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984333"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="0f037-103">\_Сообщение CPL невинкуире</span><span class="sxs-lookup"><span data-stu-id="0f037-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="0f037-104">Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления для запроса сведений о диалоговом окне, которое поддерживает приложение.</span><span class="sxs-lookup"><span data-stu-id="0f037-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f037-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f037-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f037-106">*уаппнум*</span><span class="sxs-lookup"><span data-stu-id="0f037-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="0f037-107">Число в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0f037-107">The dialog box number.</span></span> <span data-ttu-id="0f037-108">Это число должно находиться в диапазоне от нуля до значения, возвращенного в ответ на сообщение [**CPL \_ NOCOUNT**](cpl-getcount.md) (CPL \_ -count – 1).</span><span class="sxs-lookup"><span data-stu-id="0f037-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="0f037-109">*лпнкпли*</span><span class="sxs-lookup"><span data-stu-id="0f037-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="0f037-110">Адрес структуры [**невкплинфо**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) .</span><span class="sxs-lookup"><span data-stu-id="0f037-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="0f037-111">Приложение панели управления должно заполнить эту структуру сведениями о диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0f037-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f037-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f037-112">Return value</span></span>

<span data-ttu-id="0f037-113">Если функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) успешно обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="0f037-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f037-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f037-114">Remarks</span></span>

<span data-ttu-id="0f037-115">Для повышения производительности большинство приложений должны игнорировать **CPL \_ невинкуире** и обрабатывать сообщение о [**\_ запросах CPL**](cpl-inquire.md) .</span><span class="sxs-lookup"><span data-stu-id="0f037-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="0f037-116">Панель управления отправляет сообщение **CPL \_ невинкуире** один раз для каждого диалогового окна, поддерживаемого приложением.</span><span class="sxs-lookup"><span data-stu-id="0f037-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="0f037-117">Панель управления также отправляет сообщение о [**\_ запросах CPL**](cpl-inquire.md) для каждого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0f037-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="0f037-118">Эти сообщения отправляются сразу после сообщения [**CPL. \_ Count**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="0f037-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="0f037-119">Однако система не гарантирует, что порядок отправки сообщений CPL **\_ Невинкуире и CPL** . **\_**</span><span class="sxs-lookup"><span data-stu-id="0f037-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="0f037-120">При получении запроса [**CPL \_**](cpl-inquire.md)можно выполнить инициализацию этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0f037-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="0f037-121">Если необходимо выделить память, сделайте это в ответ на сообщение [**CPL \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="0f037-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="0f037-122">[**CPL \_ ЗАПРОС**](cpl-inquire.md) является предпочтительным сообщением.</span><span class="sxs-lookup"><span data-stu-id="0f037-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="0f037-123">Это обусловлено тем, что **CPL \_ невинкуире** возвращает сведения в форме, которую система не может кэшировать.</span><span class="sxs-lookup"><span data-stu-id="0f037-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="0f037-124">Следовательно, приложения, обрабатывающие **CPL \_ невинкуире** , должны загружаться каждый раз, когда на панели управления потребуются сведения, что приводит к значительному снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="0f037-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="0f037-125">Единственными приложениями, которые должны использовать **CPL \_ невинкуире** , являются те, которые требуют изменения значков или отображения строк на основе состояния компьютера.</span><span class="sxs-lookup"><span data-stu-id="0f037-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="0f037-126">В этом случае обработчик [**\_ запросов CPL**](cpl-inquire.md) должен указать \_ динамическое \_ значение Res для элементов **Идикон**, **иднаме** или **идинфо** структуры [**кплинфо**](/windows/win32/api/cpl/ns-cpl-cplinfo) вместо того, чтобы указывать допустимый идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f037-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="0f037-127">Это приводит к тому, что панель управления отправляет сообщение **CPL \_ невинкуире** каждый раз, когда ему требуется значок и отображаемые строки, что позволяет указать сведения на основе текущего состояния компьютера.</span><span class="sxs-lookup"><span data-stu-id="0f037-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="0f037-128">Разумеется, это значительно медленнее, чем использование кэшированных данных.</span><span class="sxs-lookup"><span data-stu-id="0f037-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f037-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0f037-129">Requirements</span></span>



| <span data-ttu-id="0f037-130">Требование</span><span class="sxs-lookup"><span data-stu-id="0f037-130">Requirement</span></span> | <span data-ttu-id="0f037-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0f037-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0f037-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f037-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0f037-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0f037-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0f037-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f037-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0f037-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f037-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0f037-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0f037-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f037-137"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f037-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
