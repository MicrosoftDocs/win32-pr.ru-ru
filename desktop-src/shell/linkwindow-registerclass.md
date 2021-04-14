---
description: Регистрирует класс окна, который позволяет использовать общий элемент управления SysLink в окне.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: Функция LinkWindow_RegisterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985672"
---
# <a name="linkwindow_registerclass-function"></a><span data-ttu-id="c5eed-103">Линквиндов \_ registerClass, функция</span><span class="sxs-lookup"><span data-stu-id="c5eed-103">LinkWindow\_RegisterClass function</span></span>

<span data-ttu-id="c5eed-104">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c5eed-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="c5eed-105">Он может быть изменен или недоступен в последующих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="c5eed-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="c5eed-106">Вместо этого используйте [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) .\]</span><span class="sxs-lookup"><span data-stu-id="c5eed-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) instead.\]</span></span>

<span data-ttu-id="c5eed-107">Регистрирует класс окна, который позволяет использовать общий элемент управления [Syslink](../controls/syslink-overview.md) в окне.</span><span class="sxs-lookup"><span data-stu-id="c5eed-107">Registers a window class that allows for the [SysLink](../controls/syslink-overview.md) common control to be used in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5eed-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5eed-108">Syntax</span></span>


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="c5eed-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5eed-109">Parameters</span></span>

<span data-ttu-id="c5eed-110">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="c5eed-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5eed-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5eed-111">Return value</span></span>

<span data-ttu-id="c5eed-112">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="c5eed-112">Type: **BOOL**</span></span>

<span data-ttu-id="c5eed-113">Возвращает **значение true** , если регистрация прошла успешно; В противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="c5eed-113">Returns **TRUE** if registration was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5eed-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5eed-114">Remarks</span></span>

<span data-ttu-id="c5eed-115">Эта функция не имеет связанного заголовка или файла библиотеки, поэтому она должна вызываться по порядковому значению.</span><span class="sxs-lookup"><span data-stu-id="c5eed-115">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="c5eed-116">Вызовите [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL Shell32.dll, чтобы получить маркер модуля.</span><span class="sxs-lookup"><span data-stu-id="c5eed-116">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="c5eed-117">Затем вызовите [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и порядковым номером 258, чтобы использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="c5eed-117">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 258 to use this function.</span></span>

<span data-ttu-id="c5eed-118">Используйте [**линквиндов \_ унрегистеркласс**](linkwindow-unregisterclass.md) , чтобы отменить регистрацию класса после использования.</span><span class="sxs-lookup"><span data-stu-id="c5eed-118">Use [**LinkWindow\_UnregisterClass**](linkwindow-unregisterclass.md) to unregister the class after use.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5eed-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c5eed-119">Requirements</span></span>



| <span data-ttu-id="c5eed-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c5eed-120">Requirement</span></span> | <span data-ttu-id="c5eed-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c5eed-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5eed-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5eed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c5eed-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c5eed-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5eed-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5eed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c5eed-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c5eed-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c5eed-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c5eed-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5eed-127"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c5eed-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5eed-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5eed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5eed-129">Общие сведения об элементах управления SysLink</span><span class="sxs-lookup"><span data-stu-id="c5eed-129">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
