---
description: Получает имя компьютера.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: Функция _GetComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657324"
---
# <a name="_getcomputername-function"></a><span data-ttu-id="5a82e-103">\_Функция GetComputerName</span><span class="sxs-lookup"><span data-stu-id="5a82e-103">\_GetComputerName function</span></span>

<span data-ttu-id="5a82e-104">\[Эта функция является оболочкой для функции **GetComputerName** .</span><span class="sxs-lookup"><span data-stu-id="5a82e-104">\[This function is a wrapper over the **GetComputerName** function.</span></span> <span data-ttu-id="5a82e-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="5a82e-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="5a82e-106">Приложения должны вызывать **GetComputerName** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="5a82e-106">Applications should call **GetComputerName** directly.\]</span></span>

<span data-ttu-id="5a82e-107">Получает имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="5a82e-107">Gets the computer name.</span></span> <span data-ttu-id="5a82e-108">См. [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span><span class="sxs-lookup"><span data-stu-id="5a82e-108">See [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a82e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a82e-109">Syntax</span></span>


```C++
BOOL _GetComputerName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="5a82e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a82e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a82e-111">*...*</span><span class="sxs-lookup"><span data-stu-id="5a82e-111">*...*</span></span> 
<span data-ttu-id="5a82e-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5a82e-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5a82e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5a82e-113">Requirements</span></span>



| <span data-ttu-id="5a82e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5a82e-114">Requirement</span></span> | <span data-ttu-id="5a82e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5a82e-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a82e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5a82e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="5a82e-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a82e-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a82e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a82e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a82e-119">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="5a82e-119">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
