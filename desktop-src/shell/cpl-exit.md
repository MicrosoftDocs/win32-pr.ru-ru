---
description: Отправляется один раз в функцию Кплапплет приложения панели управления до выпуска библиотеки DLL, содержащей приложение панели управления.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: Сообщение CPL_EXIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262914"
---
# <a name="cpl_exit-message"></a><span data-ttu-id="bed28-103">\_Сообщение выхода CPL</span><span class="sxs-lookup"><span data-stu-id="bed28-103">CPL\_EXIT message</span></span>

<span data-ttu-id="bed28-104">Отправляется один раз в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления до выпуска библиотеки DLL, содержащей приложение панели управления.</span><span class="sxs-lookup"><span data-stu-id="bed28-104">Sent once to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application before the DLL containing the Control Panel application is released.</span></span>

## <a name="parameters"></a><span data-ttu-id="bed28-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bed28-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bed28-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bed28-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bed28-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bed28-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bed28-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bed28-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bed28-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bed28-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bed28-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bed28-110">Return value</span></span>

<span data-ttu-id="bed28-111">Если функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) успешно обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="bed28-111">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bed28-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="bed28-112">Remarks</span></span>

<span data-ttu-id="bed28-113">Это сообщение отправляется после отправки последнего сообщения об ошибке [**CPL \_**](cpl-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="bed28-113">This message is sent after the last [**CPL\_STOP**](cpl-stop.md) message is sent.</span></span>

<span data-ttu-id="bed28-114">В ответ на это сообщение приложение панели управления должно освободить выделенную память и выполнить очистку на глобальном уровне.</span><span class="sxs-lookup"><span data-stu-id="bed28-114">In response to this message, a Control Panel application must free any memory that it has allocated and perform global-level cleanup.</span></span>

## <a name="requirements"></a><span data-ttu-id="bed28-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bed28-115">Requirements</span></span>



| <span data-ttu-id="bed28-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bed28-116">Requirement</span></span> | <span data-ttu-id="bed28-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bed28-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bed28-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bed28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bed28-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bed28-119">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bed28-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bed28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bed28-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bed28-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bed28-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bed28-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bed28-123"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bed28-123"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bed28-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bed28-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed28-125">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="bed28-125">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
