---
description: Функция Дестройхандоффтабле уничтожает таблицу, созданную с помощью Креатехандоффтабле.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Функция Дестройхандоффтабле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998408"
---
# <a name="destroyhandofftable-function"></a><span data-ttu-id="ca8eb-103">Функция Дестройхандоффтабле</span><span class="sxs-lookup"><span data-stu-id="ca8eb-103">DestroyHandoffTable function</span></span>

<span data-ttu-id="ca8eb-104">Функция **дестройхандоффтабле** уничтожает таблицу, созданную с помощью **креатехандоффтабле**.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-104">The **DestroyHandoffTable** function destroys a handoff table created with **CreateHandoffTable**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8eb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca8eb-105">Syntax</span></span>


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a><span data-ttu-id="ca8eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca8eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca8eb-107">*хтабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca8eb-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca8eb-108">Обработчик для уничтоженной перегрузки таблицы.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-108">Handle to the destroyed handoff table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca8eb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca8eb-109">Return value</span></span>

<span data-ttu-id="ca8eb-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-110">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca8eb-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ca8eb-111">Requirements</span></span>



| <span data-ttu-id="ca8eb-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ca8eb-112">Requirement</span></span> | <span data-ttu-id="ca8eb-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8eb-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8eb-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca8eb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ca8eb-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ca8eb-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ca8eb-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca8eb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ca8eb-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ca8eb-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ca8eb-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ca8eb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca8eb-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca8eb-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ca8eb-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ca8eb-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca8eb-121"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca8eb-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ca8eb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ca8eb-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca8eb-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca8eb-123"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




