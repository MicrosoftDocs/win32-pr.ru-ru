---
description: Создает или открывает файл.
ms.assetid: 2a993f45-7f87-4b9e-bccc-277477558d3c
title: Функция _CreateFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _CreateFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: becd7fed9e32385409b78e00169191a12b550e3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657133"
---
# <a name="_createfile-function"></a><span data-ttu-id="5dd40-103">\_CreateFile, функция</span><span class="sxs-lookup"><span data-stu-id="5dd40-103">\_CreateFile function</span></span>

<span data-ttu-id="5dd40-104">\[Эта функция является оболочкой для функции **CreateFile** .</span><span class="sxs-lookup"><span data-stu-id="5dd40-104">\[This function is a wrapper over the **CreateFile** function.</span></span> <span data-ttu-id="5dd40-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="5dd40-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="5dd40-106">Приложения должны вызывать **CreateFile** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="5dd40-106">Applications should call **CreateFile** directly.\]</span></span>

<span data-ttu-id="5dd40-107">Создает или открывает файл.</span><span class="sxs-lookup"><span data-stu-id="5dd40-107">Creates or opens a file.</span></span> <span data-ttu-id="5dd40-108">См. раздел [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span><span class="sxs-lookup"><span data-stu-id="5dd40-108">See [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd40-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dd40-109">Syntax</span></span>


```C++
BOOL _CreateFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="5dd40-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dd40-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd40-111">*...*</span><span class="sxs-lookup"><span data-stu-id="5dd40-111">*...*</span></span> 
<span data-ttu-id="5dd40-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5dd40-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5dd40-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5dd40-113">Requirements</span></span>



| <span data-ttu-id="5dd40-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5dd40-114">Requirement</span></span> | <span data-ttu-id="5dd40-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5dd40-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd40-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5dd40-116">DLL</span></span><br/> | <dl> <span data-ttu-id="5dd40-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dd40-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dd40-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dd40-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd40-119">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="5dd40-119">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> </dl>

 

