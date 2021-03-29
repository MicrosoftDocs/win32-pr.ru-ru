---
description: Освобождает указанные данные атрибута файла.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Функция Сдбфрифилеаттрибутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806916"
---
# <a name="sdbfreefileattributes-function"></a><span data-ttu-id="6f31b-103">Функция Сдбфрифилеаттрибутес</span><span class="sxs-lookup"><span data-stu-id="6f31b-103">SdbFreeFileAttributes function</span></span>

<span data-ttu-id="6f31b-104">Освобождает указанные данные атрибута файла.</span><span class="sxs-lookup"><span data-stu-id="6f31b-104">Frees the specified file attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f31b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f31b-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="6f31b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f31b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f31b-107">*пфилеаттрибутес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f31b-107">*pFileAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f31b-108">Структура [**аттринфо**](attrinfo.md) , возвращаемая функцией [**сдбжетфилеаттрибутес**](sdbgetfileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="6f31b-108">An [**ATTRINFO**](attrinfo.md) structure returned by the [**SdbGetFileAttributes**](sdbgetfileattributes.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f31b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f31b-109">Return value</span></span>

<span data-ttu-id="6f31b-110">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="6f31b-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f31b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6f31b-111">Requirements</span></span>



| <span data-ttu-id="6f31b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6f31b-112">Requirement</span></span> | <span data-ttu-id="6f31b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6f31b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f31b-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f31b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6f31b-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f31b-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6f31b-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f31b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6f31b-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f31b-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f31b-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6f31b-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f31b-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f31b-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f31b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f31b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f31b-121">**сдбжетфилеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="6f31b-121">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




