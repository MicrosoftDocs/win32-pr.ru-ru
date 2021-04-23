---
description: Отправляется в функцию Кплапплет приложения панели управления, когда пользователь дважды щелкает значок диалогового окна, поддерживаемого приложением.
title: Сообщение CPL_DBLCLK (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997230"
---
# <a name="cpl_dblclk-message"></a><span data-ttu-id="a837d-103">\_Сообщение CPL дблклк</span><span class="sxs-lookup"><span data-stu-id="a837d-103">CPL\_DBLCLK message</span></span>

<span data-ttu-id="a837d-104">Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления, когда пользователь дважды щелкает значок диалогового окна, поддерживаемого приложением.</span><span class="sxs-lookup"><span data-stu-id="a837d-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the user double-clicks the icon of a dialog box supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="a837d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a837d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a837d-106">*уаппнум*</span><span class="sxs-lookup"><span data-stu-id="a837d-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="a837d-107">Число в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a837d-107">The dialog box number.</span></span> <span data-ttu-id="a837d-108">Это число должно находиться в диапазоне от нуля до значения, возвращенного в ответ на сообщение [**CPL \_ NOCOUNT**](cpl-getcount.md) (CPL \_ -count – 1).</span><span class="sxs-lookup"><span data-stu-id="a837d-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="a837d-109">*лдата*</span><span class="sxs-lookup"><span data-stu-id="a837d-109">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="a837d-110">Значение, которое приложение панели управления загрузило в элемент **лпдата** в структуре [**кплинфо**](/windows/win32/api/cpl/ns-cpl-cplinfo) или [**невкплинфо**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) для этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a837d-110">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="a837d-111">Приложение загружает элемент **лпдата** в ответ на сообщение [**CPL Response \_**](cpl-inquire.md) или [**CPL \_ невинкуире**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="a837d-111">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a837d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a837d-112">Return value</span></span>

<span data-ttu-id="a837d-113">Если функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) успешно обрабатывает это сообщение, возвращаемое значение равно нулю. в противном случае он не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a837d-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, the return value is zero; otherwise, it is nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a837d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a837d-114">Remarks</span></span>

<span data-ttu-id="a837d-115">В ответ на это сообщение приложение панели управления должно отобразить соответствующее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a837d-115">In response to this message, a Control Panel application must display the corresponding dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="a837d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a837d-116">Requirements</span></span>



| <span data-ttu-id="a837d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a837d-117">Requirement</span></span> | <span data-ttu-id="a837d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a837d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a837d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a837d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a837d-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a837d-120">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a837d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a837d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a837d-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a837d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a837d-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a837d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a837d-124"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a837d-124"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a837d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a837d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a837d-126">**CPL — \_ Выбор**</span><span class="sxs-lookup"><span data-stu-id="a837d-126">**CPL\_SELECT**</span></span>](cpl-select.md)
</dt> </dl>

 

 
