---
description: Регистрирует указанную базу данных.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: Функция Сдбрегистердатабасикс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538660"
---
# <a name="sdbregisterdatabaseex-function"></a><span data-ttu-id="8106a-103">Функция Сдбрегистердатабасикс</span><span class="sxs-lookup"><span data-stu-id="8106a-103">SdbRegisterDatabaseEx function</span></span>

<span data-ttu-id="8106a-104">Регистрирует указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="8106a-104">Registers the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8106a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8106a-105">Syntax</span></span>


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="8106a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8106a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8106a-107">*псздатабасепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8106a-107">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8106a-108">Путь к базе данных.</span><span class="sxs-lookup"><span data-stu-id="8106a-108">The database path.</span></span> <span data-ttu-id="8106a-109">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8106a-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8106a-110">*двдатабасетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8106a-110">*dwDatabaseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8106a-111">Тип базы данных.</span><span class="sxs-lookup"><span data-stu-id="8106a-111">The database type.</span></span> <span data-ttu-id="8106a-112">Список значений см. в разделе [типы базы данных оболочек](shim-database-types.md) .</span><span class="sxs-lookup"><span data-stu-id="8106a-112">See [Shim Database Types](shim-database-types.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="8106a-113">*птиместамп* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8106a-113">*pTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8106a-114">Метка времени для базы данных.</span><span class="sxs-lookup"><span data-stu-id="8106a-114">The time stamp for the database.</span></span> <span data-ttu-id="8106a-115">Если этот параметр имеет **значение NULL**, используется системное время.</span><span class="sxs-lookup"><span data-stu-id="8106a-115">If this parameter is **NULL**, the system time is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8106a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8106a-116">Return value</span></span>

<span data-ttu-id="8106a-117">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="8106a-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8106a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8106a-118">Remarks</span></span>

<span data-ttu-id="8106a-119">База данных должна быть зарегистрирована, прежде чем можно будет использовать любые другие SDB-функции.</span><span class="sxs-lookup"><span data-stu-id="8106a-119">A database must be registered before you can use any other SDB functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8106a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8106a-120">Requirements</span></span>



| <span data-ttu-id="8106a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8106a-121">Requirement</span></span> | <span data-ttu-id="8106a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8106a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8106a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8106a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8106a-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8106a-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8106a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8106a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8106a-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8106a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8106a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8106a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8106a-128"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8106a-128"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8106a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8106a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8106a-130">**сдбунрегистердатабасе**</span><span class="sxs-lookup"><span data-stu-id="8106a-130">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
</dt> </dl>

 

 




