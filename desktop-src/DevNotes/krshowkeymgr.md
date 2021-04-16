---
description: Открывает диалоговое окно диспетчера ключей в пользовательском интерфейсе.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: Функция Кршовкэймгр
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665159"
---
# <a name="krshowkeymgr-function"></a><span data-ttu-id="4c09f-103">Функция Кршовкэймгр</span><span class="sxs-lookup"><span data-stu-id="4c09f-103">KRShowKeyMgr function</span></span>

<span data-ttu-id="4c09f-104">\[Эта функция включена только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c09f-104">\[This function is included only in Windows XP.</span></span> <span data-ttu-id="4c09f-105">В настоящее время она не включена ни в какую другую версию Windows, ни в одну из будущих версий Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c09f-105">It is not currently included in any other version of Windows, nor is it expected to be included in any future versions of Windows.\]</span></span>

<span data-ttu-id="4c09f-106">Открывает диалоговое окно диспетчера ключей в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="4c09f-106">Brings up the key manager dialog into the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c09f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c09f-107">Syntax</span></span>


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="4c09f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c09f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c09f-109">*хвпарент*</span><span class="sxs-lookup"><span data-stu-id="4c09f-109">*hwParent*</span></span> 
</dt> <dd>

<span data-ttu-id="4c09f-110">Маркер родительского окна диалога.</span><span class="sxs-lookup"><span data-stu-id="4c09f-110">A handle to the parent window of the dialog.</span></span> <span data-ttu-id="4c09f-111">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4c09f-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4c09f-112">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="4c09f-112">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4c09f-113">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4c09f-113">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4c09f-114">*псзкмдлине*</span><span class="sxs-lookup"><span data-stu-id="4c09f-114">*pszCmdLine*</span></span> 
</dt> <dd>

<span data-ttu-id="4c09f-115">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4c09f-115">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4c09f-116">*кмдшов*</span><span class="sxs-lookup"><span data-stu-id="4c09f-116">*CmdShow*</span></span> 
</dt> <dd>

<span data-ttu-id="4c09f-117">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4c09f-117">This parameter is not used and should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c09f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c09f-118">Return value</span></span>

<span data-ttu-id="4c09f-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4c09f-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c09f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c09f-120">Remarks</span></span>

<span data-ttu-id="4c09f-121">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4c09f-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c09f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4c09f-122">Requirements</span></span>



| <span data-ttu-id="4c09f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4c09f-123">Requirement</span></span> | <span data-ttu-id="4c09f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4c09f-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c09f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4c09f-125">DLL</span></span><br/> | <dl> <span data-ttu-id="4c09f-126"><dt>Keymgr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c09f-126"><dt>Keymgr.dll</dt></span></span> </dl> |



 

 
