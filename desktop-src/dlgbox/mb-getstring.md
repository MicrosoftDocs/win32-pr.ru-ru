---
title: Функция MB_GetString (User. h)
description: Возвращает строки для стандартных кнопок окна сообщения.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Диалоговые окна MB_GetString функции
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698964"
---
# <a name="mb_getstring-function"></a><span data-ttu-id="f69ad-104">MB, \_ функция GetString</span><span class="sxs-lookup"><span data-stu-id="f69ad-104">MB\_GetString function</span></span>

<span data-ttu-id="f69ad-105">Возвращает строки для стандартных кнопок окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="f69ad-105">Returns strings for standard message box buttons.</span></span>

## <a name="syntax"></a><span data-ttu-id="f69ad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f69ad-106">Syntax</span></span>


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a><span data-ttu-id="f69ad-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f69ad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f69ad-108">*вбтн*</span><span class="sxs-lookup"><span data-stu-id="f69ad-108">*wBtn*</span></span> 
</dt> <dd>

<span data-ttu-id="f69ad-109">Идентификатор возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="f69ad-109">The id of the string to return.</span></span> <span data-ttu-id="f69ad-110">Они определяются значениями ИДЕНТИФИКАТОРов команд диалогового окна, указанными в файле WinUser. h.</span><span class="sxs-lookup"><span data-stu-id="f69ad-110">These are identified by the Dialog Box Command ID values listed in winuser.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f69ad-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f69ad-111">Return value</span></span>

<span data-ttu-id="f69ad-112">Строка или значение NULL, если объект не найден.</span><span class="sxs-lookup"><span data-stu-id="f69ad-112">The string, or NULL if not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="f69ad-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f69ad-113">Requirements</span></span>



| <span data-ttu-id="f69ad-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f69ad-114">Requirement</span></span> | <span data-ttu-id="f69ad-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f69ad-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f69ad-116">Header</span><span class="sxs-lookup"><span data-stu-id="f69ad-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f69ad-117"><dt>User. h</dt></span><span class="sxs-lookup"><span data-stu-id="f69ad-117"><dt>User.h</dt></span></span> </dl>     |
| <span data-ttu-id="f69ad-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f69ad-118">Library</span></span><br/> | <dl> <span data-ttu-id="f69ad-119"><dt>User32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f69ad-119"><dt>User32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f69ad-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f69ad-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="f69ad-121"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f69ad-121"><dt>User32.dll</dt></span></span> </dl> |



 

 





