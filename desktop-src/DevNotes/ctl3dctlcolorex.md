---
description: Обрабатывает сообщение WM \_ ктлколор для приложений, использующих CTL3D сегодня.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Функция Ctl3dCtlColorEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648953"
---
# <a name="ctl3dctlcolorex-function"></a><span data-ttu-id="0d006-103">Функция Ctl3dCtlColorEx</span><span class="sxs-lookup"><span data-stu-id="0d006-103">Ctl3dCtlColorEx function</span></span>

<span data-ttu-id="0d006-104">Обрабатывает сообщение **WM \_ ктлколор** для приложений, использующих CTL3D сегодня.</span><span class="sxs-lookup"><span data-stu-id="0d006-104">Handles the **WM\_CTLCOLOR** message for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d006-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d006-105">Syntax</span></span>


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="0d006-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d006-107">*wm*</span><span class="sxs-lookup"><span data-stu-id="0d006-107">*wm*</span></span> 
</dt> <dd>

<span data-ttu-id="0d006-108">Сообщение **WM \_ ктлколор** для приложения.</span><span class="sxs-lookup"><span data-stu-id="0d006-108">The **WM\_CTLCOLOR** message for the application.</span></span>

</dd> <dt>

<span data-ttu-id="0d006-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d006-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d006-110">Маркер контекста отображаемого содержимого (DC).</span><span class="sxs-lookup"><span data-stu-id="0d006-110">A handle to the display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="0d006-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d006-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d006-112">Маркер дочернего окна (элемента управления).</span><span class="sxs-lookup"><span data-stu-id="0d006-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d006-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d006-113">Return value</span></span>

<span data-ttu-id="0d006-114">Возвращает дескриптор соответствующей кисти, если функция выполнена. в противном случае возвращается значение, `(HBRUSH)(0)` указывающее, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="0d006-114">Returns a handle to the appropriate brush if the function succeeds; otherwise, it returns `(HBRUSH)(0)` indicating that an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d006-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d006-115">Remarks</span></span>

<span data-ttu-id="0d006-116">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0d006-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d006-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0d006-117">Requirements</span></span>



| <span data-ttu-id="0d006-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0d006-118">Requirement</span></span> | <span data-ttu-id="0d006-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0d006-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d006-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0d006-120">DLL</span></span><br/> | <dl> <span data-ttu-id="0d006-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d006-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
