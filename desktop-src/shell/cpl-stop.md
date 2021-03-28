---
description: Отправляется в функцию Кплапплет приложения панели управления при закрытии управляющего приложения панели управления. Управляющее приложение отправляет сообщение один раз для каждого диалогового окна, которое поддерживает приложение.
title: Сообщение CPL_STOP (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984329"
---
# <a name="cpl_stop-message"></a><span data-ttu-id="ee330-104">\_Сообщение об ошибке CPL</span><span class="sxs-lookup"><span data-stu-id="ee330-104">CPL\_STOP message</span></span>

<span data-ttu-id="ee330-105">Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления при закрытии управляющего приложения панели управления.</span><span class="sxs-lookup"><span data-stu-id="ee330-105">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the controlling application of the Control Panel closes.</span></span> <span data-ttu-id="ee330-106">Управляющее приложение отправляет сообщение один раз для каждого диалогового окна, которое поддерживает приложение.</span><span class="sxs-lookup"><span data-stu-id="ee330-106">The controlling application sends the message once for each dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee330-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee330-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee330-108">*уаппнум*</span><span class="sxs-lookup"><span data-stu-id="ee330-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="ee330-109">Число в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ee330-109">The dialog box number.</span></span>

</dd> <dt>

<span data-ttu-id="ee330-110">*лдата*</span><span class="sxs-lookup"><span data-stu-id="ee330-110">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="ee330-111">Значение, которое приложение панели управления загрузило в элемент **лпдата** в структуре [**кплинфо**](/windows/win32/api/cpl/ns-cpl-cplinfo) или [**невкплинфо**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) для этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ee330-111">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="ee330-112">Приложение загружает элемент **лпдата** в ответ на сообщение [**CPL Response \_**](cpl-inquire.md) или [**CPL \_ невинкуире**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="ee330-112">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee330-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee330-113">Return value</span></span>

<span data-ttu-id="ee330-114">Если функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) успешно обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="ee330-114">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee330-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee330-115">Remarks</span></span>

<span data-ttu-id="ee330-116">В ответ на это сообщение приложение панели управления должно выполнить очистку для данного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ee330-116">In response to this message, a Control Panel application must perform cleanup for the given dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee330-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ee330-117">Requirements</span></span>



| <span data-ttu-id="ee330-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ee330-118">Requirement</span></span> | <span data-ttu-id="ee330-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ee330-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ee330-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee330-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ee330-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ee330-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ee330-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee330-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ee330-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee330-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ee330-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ee330-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee330-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee330-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee330-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee330-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee330-127">**\_выход CPL**</span><span class="sxs-lookup"><span data-stu-id="ee330-127">**CPL\_EXIT**</span></span>](cpl-exit.md)
</dt> <dt>

[<span data-ttu-id="ee330-128">**CPL — \_ Счетчик**</span><span class="sxs-lookup"><span data-stu-id="ee330-128">**CPL\_GETCOUNT**</span></span>](cpl-getcount.md)
</dt> </dl>

 

 
