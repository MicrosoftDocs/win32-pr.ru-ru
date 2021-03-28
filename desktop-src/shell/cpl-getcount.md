---
description: Отправляется в функцию Кплапплет приложения панели управления для получения количества диалоговых окон, поддерживаемых приложением.
title: Сообщение CPL_GETCOUNT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540546"
---
# <a name="cpl_getcount-message"></a><span data-ttu-id="bf038-103">\_Сообщение CPL NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="bf038-103">CPL\_GETCOUNT message</span></span>

<span data-ttu-id="bf038-104">Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления для получения количества диалоговых окон, поддерживаемых приложением.</span><span class="sxs-lookup"><span data-stu-id="bf038-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to retrieve the number of dialog boxes supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf038-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf038-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf038-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf038-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bf038-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bf038-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bf038-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf038-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bf038-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bf038-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf038-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf038-110">Return value</span></span>

<span data-ttu-id="bf038-111">Функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) возвращает число диалоговых окон, поддерживаемых приложением панели управления.</span><span class="sxs-lookup"><span data-stu-id="bf038-111">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function returns the number of dialog boxes that the Control Panel application supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf038-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf038-112">Remarks</span></span>

<span data-ttu-id="bf038-113">Это сообщение отправляется сразу после сообщения [**CPL \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="bf038-113">This message is sent immediately after the [**CPL\_INIT**](cpl-init.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf038-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bf038-114">Requirements</span></span>



| <span data-ttu-id="bf038-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bf038-115">Requirement</span></span> | <span data-ttu-id="bf038-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bf038-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bf038-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf038-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf038-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bf038-118">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bf038-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf038-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf038-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf038-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bf038-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bf038-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf038-122"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf038-122"><dt>Cpl.h</dt></span></span> </dl> |



 

 
