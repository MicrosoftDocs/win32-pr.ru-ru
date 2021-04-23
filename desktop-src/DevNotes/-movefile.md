---
description: Перемещает существующий файл или каталог, включая его дочерние элементы.
ms.assetid: 1c533b02-6674-4390-bc49-6420403778a8
title: Функция _MoveFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MoveFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 44c57d562feff62e21c4c769bfc9d6a650f4984c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656910"
---
# <a name="_movefile-function"></a><span data-ttu-id="36194-103">\_Функция MoveFile</span><span class="sxs-lookup"><span data-stu-id="36194-103">\_MoveFile function</span></span>

<span data-ttu-id="36194-104">\[Эта функция является оболочкой для функции **MoveFile** .</span><span class="sxs-lookup"><span data-stu-id="36194-104">\[This function is a wrapper over the **MoveFile** function.</span></span> <span data-ttu-id="36194-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="36194-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="36194-106">Приложения должны вызывать **MoveFile** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="36194-106">Applications should call **MoveFile** directly.\]</span></span>

<span data-ttu-id="36194-107">Перемещает существующий файл или каталог, включая его дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="36194-107">Moves an existing file or directory, including its children.</span></span> <span data-ttu-id="36194-108">См. [ **MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span><span class="sxs-lookup"><span data-stu-id="36194-108">See [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span></span>

## <a name="syntax"></a><span data-ttu-id="36194-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36194-109">Syntax</span></span>


```C++
BOOL _MoveFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="36194-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="36194-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36194-111">*...*</span><span class="sxs-lookup"><span data-stu-id="36194-111">*...*</span></span> 
<span data-ttu-id="36194-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="36194-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="36194-113">Требования</span><span class="sxs-lookup"><span data-stu-id="36194-113">Requirements</span></span>



| <span data-ttu-id="36194-114">Требование</span><span class="sxs-lookup"><span data-stu-id="36194-114">Requirement</span></span> | <span data-ttu-id="36194-115">Значение</span><span class="sxs-lookup"><span data-stu-id="36194-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36194-116">DLL</span><span class="sxs-lookup"><span data-stu-id="36194-116">DLL</span></span><br/> | <dl> <span data-ttu-id="36194-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36194-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36194-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36194-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36194-119">**MoveFile**</span><span class="sxs-lookup"><span data-stu-id="36194-119">**MoveFile**</span></span>](/windows/win32/api/winbase/nf-winbase-movefile)
</dt> </dl>

 

 
