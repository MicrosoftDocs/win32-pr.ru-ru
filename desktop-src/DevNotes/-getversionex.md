---
description: Возвращает сведения о версии операционной системы.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: Функция _GetVersionEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657020"
---
# <a name="_getversionex-function"></a><span data-ttu-id="5dd73-103">\_GetVersionEx, функция</span><span class="sxs-lookup"><span data-stu-id="5dd73-103">\_GetVersionEx function</span></span>

<span data-ttu-id="5dd73-104">\[Эта функция является оболочкой для функции **GetVersionEx** .</span><span class="sxs-lookup"><span data-stu-id="5dd73-104">\[This function is a wrapper over the **GetVersionEx** function.</span></span> <span data-ttu-id="5dd73-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="5dd73-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="5dd73-106">Приложения должны вызывать **GetVersionEx** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="5dd73-106">Applications should call **GetVersionEx** directly.\]</span></span>

<span data-ttu-id="5dd73-107">Возвращает сведения о версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5dd73-107">Gets information about the operating system version.</span></span> <span data-ttu-id="5dd73-108">См. раздел [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span><span class="sxs-lookup"><span data-stu-id="5dd73-108">See [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd73-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dd73-109">Syntax</span></span>


```C++
BOOL _GetVersionEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="5dd73-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dd73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd73-111">*...*</span><span class="sxs-lookup"><span data-stu-id="5dd73-111">*...*</span></span> 
<span data-ttu-id="5dd73-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5dd73-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5dd73-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5dd73-113">Requirements</span></span>



| <span data-ttu-id="5dd73-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5dd73-114">Requirement</span></span> | <span data-ttu-id="5dd73-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5dd73-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd73-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5dd73-116">DLL</span></span><br/> | <dl> <span data-ttu-id="5dd73-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dd73-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dd73-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dd73-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd73-119">**GetVersionEx**</span><span class="sxs-lookup"><span data-stu-id="5dd73-119">**GetVersionEx**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
