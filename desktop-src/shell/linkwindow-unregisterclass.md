---
description: Отменяет регистрацию класса окна, зарегистрированного с помощью Линквиндов \_ registerClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: Функция LinkWindow_UnregisterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985669"
---
# <a name="linkwindow_unregisterclass-function"></a><span data-ttu-id="b8ab1-103">Линквиндов \_ унрегистеркласс, функция</span><span class="sxs-lookup"><span data-stu-id="b8ab1-103">LinkWindow\_UnregisterClass function</span></span>

<span data-ttu-id="b8ab1-104">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b8ab1-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="b8ab1-105">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8ab1-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b8ab1-106">Отменяет регистрацию класса окна, зарегистрированного с помощью [**линквиндов \_ registerClass**](linkwindow-registerclass.md).</span><span class="sxs-lookup"><span data-stu-id="b8ab1-106">Unregisters a window class registered by [**LinkWindow\_RegisterClass**](linkwindow-registerclass.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ab1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8ab1-107">Syntax</span></span>


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="b8ab1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8ab1-108">Parameters</span></span>

<span data-ttu-id="b8ab1-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="b8ab1-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8ab1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8ab1-110">Return value</span></span>

<span data-ttu-id="b8ab1-111">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="b8ab1-111">Type: **BOOL**</span></span>

<span data-ttu-id="b8ab1-112">Возвращает **значение true** , если операция выполнена успешно; В противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="b8ab1-112">Returns **TRUE** if the operation was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ab1-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8ab1-113">Remarks</span></span>

<span data-ttu-id="b8ab1-114">Эта функция не имеет связанного заголовка или файла библиотеки, поэтому она должна вызываться по порядковому значению.</span><span class="sxs-lookup"><span data-stu-id="b8ab1-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="b8ab1-115">Вызовите [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL Shell32.dll, чтобы получить маркер модуля.</span><span class="sxs-lookup"><span data-stu-id="b8ab1-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="b8ab1-116">Затем вызовите [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и порядковым номером 259, чтобы использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b8ab1-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 259 to use this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ab1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b8ab1-117">Requirements</span></span>



| <span data-ttu-id="b8ab1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b8ab1-118">Requirement</span></span> | <span data-ttu-id="b8ab1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b8ab1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ab1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8ab1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ab1-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8ab1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8ab1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8ab1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ab1-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8ab1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b8ab1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b8ab1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8ab1-125"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b8ab1-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ab1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8ab1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ab1-127">Общие сведения об элементах управления SysLink</span><span class="sxs-lookup"><span data-stu-id="b8ab1-127">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
