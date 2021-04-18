---
description: Форматирует строку сообщения.
ms.assetid: e5513b0d-5f93-4bcd-a011-eb4a6fab91e1
title: Функция _FormatMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _FormatMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 27cbcfb0d69d0b4dec72834bfc8f69a9f97048ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648731"
---
# <a name="_formatmessage-function"></a><span data-ttu-id="701bf-103">\_FormatMessage, функция</span><span class="sxs-lookup"><span data-stu-id="701bf-103">\_FormatMessage function</span></span>

<span data-ttu-id="701bf-104">\[Эта функция является оболочкой для функции **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="701bf-104">\[This function is a wrapper over the **FormatMessage** function.</span></span> <span data-ttu-id="701bf-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="701bf-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="701bf-106">Приложения должны вызывать **FormatMessage** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="701bf-106">Applications should call **FormatMessage** directly.\]</span></span>

<span data-ttu-id="701bf-107">Форматирует строку сообщения.</span><span class="sxs-lookup"><span data-stu-id="701bf-107">Formats a message string.</span></span> <span data-ttu-id="701bf-108">См. раздел [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage).</span><span class="sxs-lookup"><span data-stu-id="701bf-108">See [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="701bf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="701bf-109">Syntax</span></span>


```C++
DWORD _FormatMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="701bf-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="701bf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="701bf-111">*...*</span><span class="sxs-lookup"><span data-stu-id="701bf-111">*...*</span></span> 
<span data-ttu-id="701bf-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="701bf-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="701bf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="701bf-113">Requirements</span></span>



| <span data-ttu-id="701bf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="701bf-114">Requirement</span></span> | <span data-ttu-id="701bf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="701bf-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="701bf-116">DLL</span><span class="sxs-lookup"><span data-stu-id="701bf-116">DLL</span></span><br/> | <dl> <span data-ttu-id="701bf-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="701bf-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="701bf-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="701bf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701bf-119">**FormatMessage**</span><span class="sxs-lookup"><span data-stu-id="701bf-119">**FormatMessage**</span></span>](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> </dl>

 

 
