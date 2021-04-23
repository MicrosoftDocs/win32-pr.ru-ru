---
description: Позволяет отладчику анализировать сведения о таблице динамической функции.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: Функция Ртлжетфунктионтаблелиссеад
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669032"
---
# <a name="rtlgetfunctiontablelisthead-function"></a><span data-ttu-id="1cd87-103">Функция Ртлжетфунктионтаблелиссеад</span><span class="sxs-lookup"><span data-stu-id="1cd87-103">RtlGetFunctionTableListHead function</span></span>

<span data-ttu-id="1cd87-104">\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]</span><span class="sxs-lookup"><span data-stu-id="1cd87-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="1cd87-105">Позволяет отладчику анализировать сведения о таблице динамической функции.</span><span class="sxs-lookup"><span data-stu-id="1cd87-105">Enables a debugger to examine dynamic function table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd87-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cd87-106">Syntax</span></span>


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a><span data-ttu-id="1cd87-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cd87-107">Parameters</span></span>

<span data-ttu-id="1cd87-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="1cd87-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cd87-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cd87-109">Return value</span></span>

<span data-ttu-id="1cd87-110">Возвращает указатель на заголовок списка таблиц функций.</span><span class="sxs-lookup"><span data-stu-id="1cd87-110">Returns a pointer to the head of the function table list.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cd87-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1cd87-111">Remarks</span></span>

<span data-ttu-id="1cd87-112">Обратите внимание, что для некоторых определений требуется файл заголовка Нтдеф. h для комплекта драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="1cd87-112">Note that the Windows Driver Kit (WDK) header file Ntdef.h is required for some definitions.</span></span> <span data-ttu-id="1cd87-113">Связанная библиотека импорта, NTDLL. lib, доступна в WDK.</span><span class="sxs-lookup"><span data-stu-id="1cd87-113">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="1cd87-114">Можно также использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="1cd87-114">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cd87-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1cd87-115">Requirements</span></span>



| <span data-ttu-id="1cd87-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1cd87-116">Requirement</span></span> | <span data-ttu-id="1cd87-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1cd87-117">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd87-118">DLL</span><span class="sxs-lookup"><span data-stu-id="1cd87-118">DLL</span></span><br/> | <dl> <span data-ttu-id="1cd87-119"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cd87-119"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
