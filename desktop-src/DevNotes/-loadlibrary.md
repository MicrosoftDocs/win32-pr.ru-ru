---
description: Загружает библиотеку.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: Функция _LoadLibrary
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648024"
---
# <a name="_loadlibrary-function"></a><span data-ttu-id="d297e-103">\_LoadLibrary, функция</span><span class="sxs-lookup"><span data-stu-id="d297e-103">\_LoadLibrary function</span></span>

<span data-ttu-id="d297e-104">\[Эта функция является оболочкой для функции **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="d297e-104">\[This function is a wrapper over the **LoadLibrary** function.</span></span> <span data-ttu-id="d297e-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="d297e-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="d297e-106">Приложения должны вызывать **LoadLibrary** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="d297e-106">Applications should call **LoadLibrary** directly.\]</span></span>

<span data-ttu-id="d297e-107">Загружает библиотеку.</span><span class="sxs-lookup"><span data-stu-id="d297e-107">Loads a library.</span></span> <span data-ttu-id="d297e-108">См. раздел [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="d297e-108">See [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

## <a name="syntax"></a><span data-ttu-id="d297e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d297e-109">Syntax</span></span>


```C++
HMODULE _LoadLibrary(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="d297e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d297e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d297e-111">*...*</span><span class="sxs-lookup"><span data-stu-id="d297e-111">*...*</span></span> 
<span data-ttu-id="d297e-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d297e-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d297e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d297e-113">Requirements</span></span>



| <span data-ttu-id="d297e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d297e-114">Requirement</span></span> | <span data-ttu-id="d297e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d297e-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d297e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d297e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d297e-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d297e-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d297e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d297e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d297e-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="d297e-119">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
