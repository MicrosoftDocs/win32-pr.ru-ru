---
description: Функция Жетпротоколфромнаме возвращает маркер для протокола с заданным именем.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: Функция Жетпротоколфромнаме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808705"
---
# <a name="getprotocolfromname-function"></a><span data-ttu-id="14af8-103">Функция Жетпротоколфромнаме</span><span class="sxs-lookup"><span data-stu-id="14af8-103">GetProtocolFromName function</span></span>

<span data-ttu-id="14af8-104">Функция **жетпротоколфромнаме** возвращает маркер для протокола с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="14af8-104">The **GetProtocolFromName** function returns a handle to a protocol of a given name.</span></span>

## <a name="syntax"></a><span data-ttu-id="14af8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14af8-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="14af8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14af8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14af8-107">*ProtocolName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14af8-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14af8-108">Имя протокола (например, IP).</span><span class="sxs-lookup"><span data-stu-id="14af8-108">Protocol name (for example, IP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14af8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14af8-109">Return value</span></span>

<span data-ttu-id="14af8-110">Если функция выполнена успешно, возвращаемое значение является маркером протокола.</span><span class="sxs-lookup"><span data-stu-id="14af8-110">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="14af8-111">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="14af8-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="14af8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14af8-112">Remarks</span></span>

<span data-ttu-id="14af8-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетпротоколфромнаме** .</span><span class="sxs-lookup"><span data-stu-id="14af8-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolFromName** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14af8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="14af8-114">Requirements</span></span>



| <span data-ttu-id="14af8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="14af8-115">Requirement</span></span> | <span data-ttu-id="14af8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="14af8-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14af8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14af8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14af8-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14af8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="14af8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14af8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14af8-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14af8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="14af8-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14af8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14af8-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="14af8-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="14af8-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14af8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="14af8-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14af8-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="14af8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="14af8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14af8-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14af8-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




