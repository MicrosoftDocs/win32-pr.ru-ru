---
description: Отменяет регистрацию указанной базы данных и делает ее более недоступной.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: Функция Сдбунрегистердатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496092"
---
# <a name="sdbunregisterdatabase-function"></a><span data-ttu-id="bcf20-103">Функция Сдбунрегистердатабасе</span><span class="sxs-lookup"><span data-stu-id="bcf20-103">SdbUnregisterDatabase function</span></span>

<span data-ttu-id="bcf20-104">Отменяет регистрацию указанной базы данных и делает ее более недоступной.</span><span class="sxs-lookup"><span data-stu-id="bcf20-104">Unregisters the specified database, making it no longer available.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcf20-105">Syntax</span></span>


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a><span data-ttu-id="bcf20-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcf20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf20-107">*пгуиддб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcf20-107">*pguidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf20-108">Идентификатор GUID базы данных.</span><span class="sxs-lookup"><span data-stu-id="bcf20-108">The GUID of the database.</span></span> <span data-ttu-id="bcf20-109">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bcf20-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf20-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcf20-110">Return value</span></span>

<span data-ttu-id="bcf20-111">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="bcf20-111">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf20-112">Требования</span><span class="sxs-lookup"><span data-stu-id="bcf20-112">Requirements</span></span>



| <span data-ttu-id="bcf20-113">Требование</span><span class="sxs-lookup"><span data-stu-id="bcf20-113">Requirement</span></span> | <span data-ttu-id="bcf20-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bcf20-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf20-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcf20-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf20-116">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bcf20-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bcf20-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcf20-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf20-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bcf20-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bcf20-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf20-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf20-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf20-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf20-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcf20-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf20-122">**сдбрегистердатабасикс**</span><span class="sxs-lookup"><span data-stu-id="bcf20-122">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




