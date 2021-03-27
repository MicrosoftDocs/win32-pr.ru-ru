---
description: Отправляется в функцию Кплапплет приложения панели управления для запроса сведений о диалоговом окне, которое поддерживает приложение.
title: Сообщение CPL_INQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f4c75a2610dab9e94a97eb7920c9de43cf44efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143972"
---
# <a name="cpl_inquire-message"></a><span data-ttu-id="a6a7f-103">\_Сообщение о запросах CPL</span><span class="sxs-lookup"><span data-stu-id="a6a7f-103">CPL\_INQUIRE message</span></span>

<span data-ttu-id="a6a7f-104">Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления для запроса сведений о диалоговом окне, которое поддерживает приложение.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6a7f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6a7f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a7f-106">*уаппнум*</span><span class="sxs-lookup"><span data-stu-id="a6a7f-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a7f-107">Число в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-107">The dialog box number.</span></span> <span data-ttu-id="a6a7f-108">Это число должно находиться в диапазоне от нуля до значения, возвращенного в ответ на сообщение [**CPL \_ NOCOUNT**](cpl-getcount.md) (CPL \_ -count – 1).</span><span class="sxs-lookup"><span data-stu-id="a6a7f-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="a6a7f-109">*лпкпли*</span><span class="sxs-lookup"><span data-stu-id="a6a7f-109">*lpcpli*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a7f-110">Адрес структуры [**кплинфо**](/windows/win32/api/cpl/ns-cpl-cplinfo) .</span><span class="sxs-lookup"><span data-stu-id="a6a7f-110">The address of a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure.</span></span> <span data-ttu-id="a6a7f-111">Приложение должно заполнить эту структуру идентификаторами ресурсов для значка, краткого имени, описания и любого определяемого пользователем значения, связанного с этим диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-111">The application must fill this structure with resource identifiers for the icon, short name, description, and any user-defined value associated with the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a7f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6a7f-112">Return value</span></span>

<span data-ttu-id="a6a7f-113">Если функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) успешно обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a7f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6a7f-114">Remarks</span></span>

<span data-ttu-id="a6a7f-115">Панель управления отправляет сообщение " **\_ запрос CPL** " один раз для каждого диалогового окна, поддерживаемого приложением.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-115">The Control Panel sends the **CPL\_INQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="a6a7f-116">Панель управления также отправляет сообщение [**CPL \_ невинкуире**](cpl-newinquire.md) для каждого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-116">The Control Panel also sends a [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message for each dialog box.</span></span> <span data-ttu-id="a6a7f-117">Эти сообщения отправляются сразу после сообщения [**CPL. \_ Count**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a7f-117">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="a6a7f-118">Однако система не гарантирует, что порядок отправки сообщений CPL **\_ Невинкуире и CPL** . **\_**</span><span class="sxs-lookup"><span data-stu-id="a6a7f-118">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="a6a7f-119">При получении запроса **CPL \_** можно выполнить инициализацию этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-119">You can perform initialization for the dialog box when you receive **CPL\_INQUIRE**.</span></span> <span data-ttu-id="a6a7f-120">Если необходимо выделить память, сделайте это в ответ на сообщение [**CPL \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a7f-120">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="a6a7f-121">Сообщение [**CPL \_ невинкуире**](cpl-newinquire.md) возвращает сведения в форме, которую система не может кэшировать.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-121">The [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="a6a7f-122">По этой причине большинство функций [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) должны обрабатывать **CPL с \_ запросом** и игнорировать **CPL \_ невинкуире**.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-122">For this reason, most [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) functions should process **CPL\_INQUIRE** and ignore **CPL\_NEWINQUIRE**.</span></span>

<span data-ttu-id="a6a7f-123">Единственными приложениями, которые должны использовать [**CPL \_ невинкуире**](cpl-newinquire.md) , являются те, которые требуют изменения значков или отображения строк на основе состояния компьютера.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-123">The only applications that should use [**CPL\_NEWINQUIRE**](cpl-newinquire.md) are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="a6a7f-124">В этом случае обработчик **\_ запросов CPL** должен указать \_ динамическое \_ значение Res для элементов **Идикон**, **иднаме** или **идинфо** структуры [**кплинфо**](/windows/win32/api/cpl/ns-cpl-cplinfo) вместо того, чтобы указывать допустимый идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-124">In this case, your **CPL\_INQUIRE** handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="a6a7f-125">Это приводит к тому, что панель управления отправляет сообщение **CPL \_ невинкуире** каждый раз, когда ему требуется значок и отображаемые строки, что позволяет указать сведения на основе текущего состояния компьютера.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-125">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="a6a7f-126">Это значительно медленнее, чем использование кэшированных данных.</span><span class="sxs-lookup"><span data-stu-id="a6a7f-126">This is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a7f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a6a7f-127">Requirements</span></span>



| <span data-ttu-id="a6a7f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a6a7f-128">Requirement</span></span> | <span data-ttu-id="a6a7f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a6a7f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a6a7f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6a7f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a7f-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6a7f-131">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a6a7f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6a7f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a7f-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a6a7f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a6a7f-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a6a7f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a7f-135"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a7f-135"><dt>Cpl.h</dt></span></span> </dl> |



 

 
