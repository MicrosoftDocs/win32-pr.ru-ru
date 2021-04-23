---
description: Возвращает свободное место на диске.
ms.assetid: 4b7f4938-9918-4625-b28d-faf22de56976
title: Функция _GetDiskFreeSpaceEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetDiskFreeSpaceEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
ms.openlocfilehash: da4a8eefabf03f6330ac9c1f135482f27dd8aa18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649020"
---
# <a name="_getdiskfreespaceex-function"></a><span data-ttu-id="e7e3b-103">\_Функция Жетдискфриспацеекс</span><span class="sxs-lookup"><span data-stu-id="e7e3b-103">\_GetDiskFreeSpaceEx function</span></span>

<span data-ttu-id="e7e3b-104">\[Эта функция является оболочкой для функции **жетдискфриспацеекс** .</span><span class="sxs-lookup"><span data-stu-id="e7e3b-104">\[This function is a wrapper over the **GetDiskFreeSpaceEx** function.</span></span> <span data-ttu-id="e7e3b-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="e7e3b-106">Приложения должны вызывать **жетдискфриспацеекс** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="e7e3b-106">Applications should call **GetDiskFreeSpaceEx** directly.\]</span></span>

<span data-ttu-id="e7e3b-107">Возвращает свободное место на диске.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-107">Gets the free disk space.</span></span> <span data-ttu-id="e7e3b-108">См. [**жетдискфриспацеекс**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span><span class="sxs-lookup"><span data-stu-id="e7e3b-108">See [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e3b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7e3b-109">Syntax</span></span>


```C++
BOOL _GetDiskFreeSpaceEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="e7e3b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7e3b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e3b-111">*...*</span><span class="sxs-lookup"><span data-stu-id="e7e3b-111">*...*</span></span> 
<span data-ttu-id="e7e3b-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e7e3b-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e7e3b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e7e3b-113">Requirements</span></span>



| <span data-ttu-id="e7e3b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e7e3b-114">Requirement</span></span> | <span data-ttu-id="e7e3b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e3b-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e3b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e3b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="e7e3b-117"><dt>Msmdun80.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e3b-117"><dt>Msmdun80.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e3b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7e3b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e3b-119">**жетдискфриспацеекс**</span><span class="sxs-lookup"><span data-stu-id="e7e3b-119">**GetDiskFreeSpaceEx**</span></span>](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa)
</dt> </dl>

 

 
