---
description: Возвращает имя пользователя.
ms.assetid: 1373fc9d-ab1c-49b9-8b82-de2e99c4821c
title: Функция _GetUserName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetUserName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: f61be4596c5076dd7763ed171124888382f3ef6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648031"
---
# <a name="_getusername-function"></a><span data-ttu-id="dc848-103">\_Функция UserName</span><span class="sxs-lookup"><span data-stu-id="dc848-103">\_GetUserName function</span></span>

<span data-ttu-id="dc848-104">\[Эта функция является оболочкой для функции- **имени пользователя** .</span><span class="sxs-lookup"><span data-stu-id="dc848-104">\[This function is a wrapper over the **GetUserName** function.</span></span> <span data-ttu-id="dc848-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="dc848-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="dc848-106">Приложения должны вызывать метод. **username** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="dc848-106">Applications should call **GetUserName** directly.\]</span></span>

<span data-ttu-id="dc848-107">Возвращает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc848-107">Gets the user name.</span></span> <span data-ttu-id="dc848-108">См. [**имя пользователя**](/windows/win32/api/winbase/nf-winbase-getusernamea).</span><span class="sxs-lookup"><span data-stu-id="dc848-108">See [**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc848-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc848-109">Syntax</span></span>


```C++
BOOL _GetUserName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="dc848-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc848-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc848-111">*...*</span><span class="sxs-lookup"><span data-stu-id="dc848-111">*...*</span></span> 
<span data-ttu-id="dc848-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc848-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dc848-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dc848-113">Requirements</span></span>



| <span data-ttu-id="dc848-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dc848-114">Requirement</span></span> | <span data-ttu-id="dc848-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dc848-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc848-116">DLL</span><span class="sxs-lookup"><span data-stu-id="dc848-116">DLL</span></span><br/> | <dl> <span data-ttu-id="dc848-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc848-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc848-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc848-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc848-119">**GetUserName**</span><span class="sxs-lookup"><span data-stu-id="dc848-119">**GetUserName**</span></span>](/windows/win32/api/winbase/nf-winbase-getusernamea)
</dt> </dl>

 

 
