---
description: Отправляется в функцию Кплапплет приложения панели управления, чтобы предложить ему выполнить глобальную инициализацию, особенно выделение памяти.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Сообщение CPL_INIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984337"
---
# <a name="cpl_init-message"></a><span data-ttu-id="e2685-103">\_Сообщение об инициализации CPL</span><span class="sxs-lookup"><span data-stu-id="e2685-103">CPL\_INIT message</span></span>

<span data-ttu-id="e2685-104">Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления, чтобы предложить ему выполнить глобальную инициализацию, особенно выделение памяти.</span><span class="sxs-lookup"><span data-stu-id="e2685-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to prompt it to perform global initialization, especially memory allocation.</span></span>


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a><span data-ttu-id="e2685-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2685-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2685-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2685-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e2685-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e2685-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e2685-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2685-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e2685-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e2685-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2685-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2685-110">Return value</span></span>

<span data-ttu-id="e2685-111">Если инициализация прошла удачно, функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) должна вернуть ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e2685-111">If initialization succeeds, the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function should return nonzero.</span></span> <span data-ttu-id="e2685-112">В противном случае он должен вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="e2685-112">Otherwise, it should return zero.</span></span>

<span data-ttu-id="e2685-113">Если [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) возвращает ноль, то управляющее приложение завершает обмен данными и освобождает библиотеку DLL, содержащую приложение панели управления.</span><span class="sxs-lookup"><span data-stu-id="e2685-113">If [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) returns zero, the controlling application ends communication and releases the DLL containing the Control Panel application.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2685-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2685-114">Remarks</span></span>

<span data-ttu-id="e2685-115">Поскольку это единственный способ, которым приложение панели управления может сообщить об ошибке, приложение должно выделить память в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="e2685-115">Because this is the only way a Control Panel application can signal an error condition, the application should allocate memory in response to this message.</span></span>

<span data-ttu-id="e2685-116">Это сообщение отправляется сразу после загрузки библиотеки DLL, содержащей приложение.</span><span class="sxs-lookup"><span data-stu-id="e2685-116">This message is sent immediately after the DLL containing the application is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2685-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e2685-117">Requirements</span></span>



| <span data-ttu-id="e2685-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e2685-118">Requirement</span></span> | <span data-ttu-id="e2685-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e2685-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e2685-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2685-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2685-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e2685-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e2685-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2685-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2685-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e2685-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e2685-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e2685-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2685-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2685-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2685-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2685-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2685-127">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="e2685-127">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
