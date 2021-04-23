---
description: Извлекает отображаемое имя указанного ТЕГА.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: Функция Сдбтагтостринг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496095"
---
# <a name="sdbtagtostring-function"></a><span data-ttu-id="8061a-103">Функция Сдбтагтостринг</span><span class="sxs-lookup"><span data-stu-id="8061a-103">SdbTagToString function</span></span>

<span data-ttu-id="8061a-104">Извлекает отображаемое имя указанного ТЕГА.</span><span class="sxs-lookup"><span data-stu-id="8061a-104">Retrieves the display name of the specified TAG.</span></span>

## <a name="syntax"></a><span data-ttu-id="8061a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8061a-105">Syntax</span></span>


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a><span data-ttu-id="8061a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8061a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8061a-107">*тег* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8061a-107">*tag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8061a-108">ТЕГ.</span><span class="sxs-lookup"><span data-stu-id="8061a-108">The TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8061a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8061a-109">Return value</span></span>

<span data-ttu-id="8061a-110">Функция возвращает указатель на строку, завершающуюся нулем, или "Инвалидтаг".</span><span class="sxs-lookup"><span data-stu-id="8061a-110">The function returns a pointer to the null-terminated string or "InvalidTag".</span></span>

## <a name="requirements"></a><span data-ttu-id="8061a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="8061a-111">Requirements</span></span>



| <span data-ttu-id="8061a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="8061a-112">Requirement</span></span> | <span data-ttu-id="8061a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8061a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8061a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8061a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8061a-115">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8061a-115">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8061a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8061a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8061a-117">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8061a-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8061a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="8061a-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8061a-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8061a-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8061a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8061a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8061a-121">**ТЕГАМИ**</span><span class="sxs-lookup"><span data-stu-id="8061a-121">**TAG**</span></span>](tag.md)
</dt> </dl>

 

 




