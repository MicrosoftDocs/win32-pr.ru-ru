---
description: Возвращает путь к модулю.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: Функция _GetModuleFileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657882"
---
# <a name="_getmodulefilename-function"></a><span data-ttu-id="a4669-103">\_Функция GetModuleFileName</span><span class="sxs-lookup"><span data-stu-id="a4669-103">\_GetModuleFileName function</span></span>

<span data-ttu-id="a4669-104">\[Эта функция является оболочкой для функции **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="a4669-104">\[This function is a wrapper over the **GetModuleFileName** function.</span></span> <span data-ttu-id="a4669-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="a4669-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="a4669-106">Приложения должны вызывать **GetModuleFileName** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="a4669-106">Applications should call **GetModuleFileName** directly.\]</span></span>

<span data-ttu-id="a4669-107">Возвращает путь к модулю.</span><span class="sxs-lookup"><span data-stu-id="a4669-107">Gets the module path.</span></span> <span data-ttu-id="a4669-108">См. [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span><span class="sxs-lookup"><span data-stu-id="a4669-108">See [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4669-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4669-109">Syntax</span></span>


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="a4669-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4669-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4669-111">*...*</span><span class="sxs-lookup"><span data-stu-id="a4669-111">*...*</span></span> 
<span data-ttu-id="a4669-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a4669-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a4669-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a4669-113">Requirements</span></span>



| <span data-ttu-id="a4669-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a4669-114">Requirement</span></span> | <span data-ttu-id="a4669-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a4669-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4669-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a4669-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a4669-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4669-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4669-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4669-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4669-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="a4669-119">**GetModuleFileName**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
