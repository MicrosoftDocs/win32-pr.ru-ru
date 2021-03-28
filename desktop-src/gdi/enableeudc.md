---
description: Эта функция включает или отключает поддержку определяемых пользователем символов (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: Функция Енаблиудк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984976"
---
# <a name="enableeudc-function"></a><span data-ttu-id="bb870-103">Функция Енаблиудк</span><span class="sxs-lookup"><span data-stu-id="bb870-103">EnableEUDC function</span></span>

<span data-ttu-id="bb870-104">Эта функция включает или отключает поддержку определяемых пользователем символов (EUDC).</span><span class="sxs-lookup"><span data-stu-id="bb870-104">This function enables or disables support for end-user-defined characters (EUDC).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb870-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb870-105">Syntax</span></span>


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a><span data-ttu-id="bb870-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb870-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb870-107">*фенаблиудк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb870-107">*fEnableEUDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb870-108">Логическое значение, равное **true** , чтобы включить EUDC, и **значение false** , чтобы отключить EUDC.</span><span class="sxs-lookup"><span data-stu-id="bb870-108">Boolean that is set to **TRUE** to enable EUDC, and to **FALSE** to disable EUDC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb870-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb870-109">Return value</span></span>

<span data-ttu-id="bb870-110">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="bb870-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="bb870-111">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="bb870-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb870-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="bb870-112">Remarks</span></span>

<span data-ttu-id="bb870-113">Если значение EUDC отключено, попытка отобразить символы EUDC приведет к отсутствующим или неправильным глифам.</span><span class="sxs-lookup"><span data-stu-id="bb870-113">If EUDC is disabled, trying to display EUDC characters will result in missing or bad glyphs.</span></span>

<span data-ttu-id="bb870-114">Во время нескольких сеансов эта функция влияет только на текущий сеанс.</span><span class="sxs-lookup"><span data-stu-id="bb870-114">During multi-session, this function affects the current session only.</span></span>

<span data-ttu-id="bb870-115">Рекомендуется использовать эту функцию в Windows XP с пакетом обновления 2 (SP2) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bb870-115">It is recommended that you use this function with Windows XP SP2 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb870-116">Требования</span><span class="sxs-lookup"><span data-stu-id="bb870-116">Requirements</span></span>



| <span data-ttu-id="bb870-117">Требование</span><span class="sxs-lookup"><span data-stu-id="bb870-117">Requirement</span></span> | <span data-ttu-id="bb870-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bb870-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb870-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb870-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb870-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb870-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bb870-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb870-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb870-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb870-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bb870-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb870-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb870-124"><dt>GDI32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb870-124"><dt>Gdi32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb870-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bb870-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb870-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb870-126"><dt>Gdi32.dll</dt></span></span> </dl> |



 

 




