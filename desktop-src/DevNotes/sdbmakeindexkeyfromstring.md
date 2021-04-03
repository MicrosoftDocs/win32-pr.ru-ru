---
description: Создает ключ из строки.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Функция Сдбмакеиндекскэйфромстринг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990306"
---
# <a name="sdbmakeindexkeyfromstring-function"></a><span data-ttu-id="0efa1-103">Функция Сдбмакеиндекскэйфромстринг</span><span class="sxs-lookup"><span data-stu-id="0efa1-103">SdbMakeIndexKeyFromString function</span></span>

<span data-ttu-id="0efa1-104">Создает ключ из строки.</span><span class="sxs-lookup"><span data-stu-id="0efa1-104">Creates a key from a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efa1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0efa1-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a><span data-ttu-id="0efa1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0efa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0efa1-107">*пвсзкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0efa1-107">*pwszKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0efa1-108">Строка.</span><span class="sxs-lookup"><span data-stu-id="0efa1-108">The string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0efa1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0efa1-109">Return value</span></span>

<span data-ttu-id="0efa1-110">Функция возвращает ключ или значение 0, если возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="0efa1-110">The function returns the key or 0 if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0efa1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0efa1-111">Remarks</span></span>

<span data-ttu-id="0efa1-112">Стандартный ключ индекса — первые восемь символов строки, преобразованный в верхний регистр, а затем приведенный к значению **улонглонг** .</span><span class="sxs-lookup"><span data-stu-id="0efa1-112">The standard index key is the first eight characters of the string, converted to upper case, then cast to a **ULONGLONG** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0efa1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0efa1-113">Requirements</span></span>



| <span data-ttu-id="0efa1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0efa1-114">Requirement</span></span> | <span data-ttu-id="0efa1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0efa1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0efa1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0efa1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0efa1-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0efa1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0efa1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0efa1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0efa1-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0efa1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0efa1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0efa1-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0efa1-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0efa1-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




